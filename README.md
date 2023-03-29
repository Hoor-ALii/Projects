### MY Projects
simple Supermarket cpp project
#include <bits/stdc++.h>
using namespace std;
class Items{
public:
    Items(){
    }
virtual void display_items()=0;

};
class SuperMarket: public Items
{
    map<int, string>product = { {1,"Vegetables and Fruits"},{2,"Bakery"},
    {3,"Drinks"},{4,"Canned Food"},{5,"Detergent"},{6,"cereals"},{7,"Meat"} };
public:
    int choose;
    SuperMarket()
    {
        display_items();
        cin >> choose;
    }
    void display_items()
    {
        cout << "Enter Department You Want To Choose From " << endl;
        for (auto x : product) {
            cout << x.first << " " << x.second << '\n';
        };

    }
};
class Vegetables_and_Fruits:public Items
{
    int choice;
    map<int, string> veg_and_fruit = { {1,"kilo Tometo : 6.0 EGP" },
         {2,"kilo Banana : 26 EGP" } ,{3,"kilo Poteto : 8.0 EGP" }
         ,{4,"kilo Apple : 40.0 EGP" } ,{5,"kilo Orange : 14.0 EGP" } };
          string name, ad, phonenumber;
public:
    void display_items()
    {
        cout << "Please Choose Your Products From The List Below :" << endl;
        for (auto x : veg_and_fruit)
        {
            cout << x.first << " " << x.second  << '\n';
        }
        cin >> choice;
    }
//=========================================================================
void dataofcustomer()
{

    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<veg_and_fruit[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================

};
class Bakery:public Items
{
     int choice;
    map<int, string>bakery = { {1,"milk Toast -500 gm- : 32.0 EGP"},
    {2,"Bread-250 gm- : 14.0 EGP" },
    {3,"fino Bread-4 pieces- : 15.0 EGP" },
    {4,"waffle-1 piece- : 9.0 EGP" },
    {5,"toast-2 pieces- : 39.0 EGP"} };
        string name, ad, phonenumber;

public:
    Bakery() {
    }
    void display_items() {
        cout << "Please Choose Your Products From The Bakery List Below :" << endl;
        for (auto x : bakery)
        {
            cout << x.first << " " << x.second  << '\n';
        }
        cin >> choice;
    };
    void dataofcustomer()
{

    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<bakery[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
};
class Drinks:public Items
{
    int choice;
    map<int, string>drinks = { {1,"Lipton Yellow Label Rich Black Tea - 100 TeaBags - 200gm : 66.0 EGP"} ,
        { 2,"Tang Pineapple Juice Powder – 25gm – : 4.75 EGP" } ,
 { 3,"Solo Pure Cocoa Powder - 400g : 121.0 EGP" } ,
{4,"Schweppes Peach Cans – 330 Ml – : 4.75 EGP" } ,
{5,"Flo Water - 600ml - : 6.5 EGP" } };
    string name, ad, phonenumber;

public:
    void display_items() {
        cout << "Please Choose Your Drink From The List Below :" << endl;
        for (auto x : drinks) {
            cout << x.first << " " << x.second  << '\n';
        }
        cin >> choice;
    }
        //=========================================================================
void dataofcustomer()
{
    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<drinks[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
    };
    class Cereals:public Items
    {
            int choice;
        map<int, string>cereals = { {1,"kilo Rice :  73.95 EGP"} ,
        {2,"1/2 kilo Pasta : 8.5 EGP" } ,
        {3,"1/2 kilo Lentils : 34.0 EGP" } ,
        {4,"1/2 kilo Beans : 36.0 EGP" } ,
        {5,"kilo Popcorn : 13.0 EGP" } };
            string name, ad, phonenumber;

    public:
        void display_items()
        {
            cout << "Please Choose Your Products From The List Below :" << endl;
            for (auto x : cereals)
            {
                cout << x.first << " " << x.second << '\n';
            }
            cin >> choice;

        }
//=========================================================================
void dataofcustomer()
{
    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<cereals[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
    };

    class Meat:public Items
    {
             int choice;
        map<int, string>meat = { {1,"kilo Burger : 179.99 EGP"} ,
        {2,"kilo sausage : 238.99 EGP " } ,
        {3,"kilo minced meat : 204.99  EGP " } ,
        {4,"kilo kofta : 119.95  EGP " } ,
        {5,"kilo chiken breast slices : 120.0 EGP" } };
            string name, ad, phonenumber;

    public:
        void display_items()
        {
            cout << "Please Choose Your Products From The List Below :" << endl;
            for (auto x : meat)
            {
                cout << x.first << " " << x.second << '\n';
            }
            cin >> choice;

        }
        //=========================================================================
void dataofcustomer()
{
    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<meat[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
        };
        class Canned_food:public Items
        {
            int choice;
            map<int, string>canned_food = { {1,"1 piece Tuna : 30.0 EGP "} ,
            {2,"1/2 kilo butter : 105.0 EGP" } ,
            {3,"1/2 kilo flour sweetness : 54.5 EGP " } ,
            {4,"3/4 kilo suger : 20.0 EGP  " } ,
            {5,"oil - 800m : 100.0 EGP " } };
                string name, ad, phonenumber;

        public:
            void display_items()
            {
                cout << "Please Choose Your Products From The List Below :" << endl;
                for (auto x : canned_food)
                {
                    cout << x.first << " " << x.second << '\n';
                }
                cin >> choice;

            }
            //=========================================================================
void dataofcustomer()
{
    cout << "\nPLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "\nPLEASE ENTER YOUR ADDRESS \n"; cin >> ad;
    cout << "PLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<canned_food[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
            };

            class Detergent:public Items
            {
                int choice;
                map<int, string>detergent = { {1,"Dettol Antiseptic Antibacterial Disinfectant Liquid – 120ml : 20.0 EGP" },
               {2, "Clenex-550- : 20.0 EGP"},
               {3, "Shampoo Clear -180ml - : 27.0 EGP"},
               {4, "Pril DishWasher - : 6.0 EGP"},
               {5, "Fragrant-1000ml- : 30.00 EGP"}
                };
                    string name, ad, phonenumber;
            public:
                void display_items()
                {
                    cout << "Please Choose Your Products From The List Below :" << endl;
                    for (auto x : detergent)
                    {
                        cout << x.first << " " << x.second << '\n';
                    }
                    cin >> choice;

                }
//=========================================================================
void dataofcustomer()
{
    cout << "PLEASE ENTER YOUR NAME AGAIN\n"; cin >> name;
    cout << "PLEASE ENTER YOUR ADDRESS\n"; cin >> ad;
    cout << "\nPLEASE ENTER YOUR PHONE NUMBER\n"; cin >> phonenumber;
    cout <<endl<< "======================================================\n" ;
    cout << "                         CASH RECEIPT:                        \n";
    cout << "======================================================\n";
    cout << "Dear customer, your purchases : "<< endl;
    cout<<"~~"<<detergent[choice]<<"~~"<<endl;
    cout << "======================================================\n";
    cout << "*Customer Data : " << endl;
     cout << "======================================================\n";
    cout << " ~Name : " << name << endl;
    cout << " ~Address : " << ad << endl;
    cout << " ~Phone Number : " << phonenumber << endl;
    cout << "======================================================\n";
    cout << "***Thank You For Choosing Us,We Hope To See You Again***\n";
    cout << endl;
    cout << "\t Our Phone Number to contact us : " << "01275127415" << endl;
      cout << "======================================================\n" << endl;
}
//===========================================================================
           };

            class Products : public SuperMarket, Vegetables_and_Fruits, Drinks,Bakery,Canned_food,Cereals,Meat ,Detergent
            {
            public:
                int ch;
                Products()
                  {
                    department();
                  }
                void department()
                 {
                    ch = choose;
                    if (ch == 1)
                    {
                        Vegetables_and_Fruits* a = new Vegetables_and_Fruits();
                        a->display_items();
                        a->dataofcustomer();
                    }
                    else
                        if (ch == 2)
                        {
                            Bakery b;
                            b.display_items();
                            b.dataofcustomer();
                        }
                        else
                            if (ch == 3)
                            {
                                Drinks c;
                                c.display_items();
                                c.dataofcustomer();
                            }
                        else
                            if (ch == 4)
                           {
                             Canned_food f;
                             f.display_items();
                             f.dataofcustomer();
                            }

                        else
                            if (ch == 5)
                           {
                             Detergent g;
                             g.display_items();
                             g.dataofcustomer();
                            }
                        else
                             if (ch == 6)
                            {
                                    Cereals d;
                                    d.display_items();
                                    d.dataofcustomer();
                            }

                        else
                            if (ch == 7)
                           {
                                        Meat e;
                                        e.display_items();
                                        e.dataofcustomer();
                            }
                 }

            };
            void welcome()
            {
                string name;
                cout << "Welcome! Please Enter Your Name\n";cin >> name;
                cout << "WELCOME BACK DEAR " << name << endl;
            }

            int main()
            {
                int total = 0;
                string ans;
                welcome();
                cout << "would you like to start shopping YES/NO : ";
                cin >> ans;
                transform(ans.begin(), ans.end(), ans.begin(), ::tolower);
                if (ans == "yes")
                {
                    Products obj1;
                }
                else
                {
                    return 0;
                }
            }
