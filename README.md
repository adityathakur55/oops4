# oops4

//program to display all your watches collection using class,constructor,inheritance,virtual function,operator overloading.





#include<iostream>
using namespace std;
class watches {
	public:
	int no,balance,wdr;
	char brand[25];

	virtual void info(){
		cout<<"enter total no of watches :"<<endl;
		cin>>no;
		cout<<"enter the balance u have in your account:"<<endl;
		cin>>balance;
		cout<<"enter amount to withdraw to buy a watches:"<<endl;
		cin>>wdr;
	
		
	}
  virtual void show(){
  	cout<<" total no of watches are:"<<no<<endl;
  	cout <<"balance u have in your account is:"<<balance<<endl;
  	cout<<"amount to withdraw:"<<wdr<<endl;
  }
  virtual void data() 
{
	cout<< "Displaying data using virtual function";
}
  
};
class sonata:public watches {
	int timex,fastrack,no,balance,wdr;
	public:
		int watches(int n){
		int titan;
		cout<<"total no. of titan's u have with u:"<<titan<<endl;
		
	}

	void info(){
		cout<<"enter total no of watches :"<<endl;
		cin>>no;
		cout<<"enter the balance u have in your account:"<<endl;
		cin>>balance;
		cout<<"enter amount to withdraw to buy watches:"<<endl;
		cin>>wdr;
	
		
	}
 	void data()
	{
 		cout<<"enter no. of timex u have"<<endl;
 		cin>>timex;
 		cout<<"enter no. of fastrack u have"<<endl;
 		cin>>fastrack;
 	}
   	void show()
	{
  		cout<<" total no of watches are:"<<no<<endl;
  		cout <<"balance u have in your account is:"<<balance<<endl;
  		cout<<"amount to withdraw:"<<wdr<<endl;
  	}
 	sonata operator + (sonata bb){
 		sonata cc;
 		cc.timex=timex+bb.timex;
 		return cc;
 	}
 
};

int main()
{
	watches *str;
	sonata pp;
	str=&pp;
	str->data();
	str->info();
	sonata aa;
	str=&aa;
	str->data();
	str->info();
	sonata cc;
	cc=pp+aa;
	cc.show();
	return 0;
}
