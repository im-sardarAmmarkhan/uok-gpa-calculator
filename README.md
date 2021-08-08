# uok-gpa-calculator
#include<iostream>
#include<stdlib.h>
using namespace std;

int main()
{
	
	int programControl=1;
	int total_marks;
	char grade;
	float total_Gpa;
	int credithour1,credithour2,credithour3,credithour4,credithour5;
	float subject1,subject2,subject3,subject4,subject5;
	int gradescores,Subject_marks;
	int choice;
	float percentage;
	while (programControl==1)
	{
	system("cls");
	cout<<"press 1 to calculate the grade and gpa of subject"<<endl;
	cout<<"press 2 to calculate the gpa of semester"<<endl;
	cin>>choice;
	switch(choice)
	{
		case 1:
			cout<<"Enter the total marks ="<<endl;
			cin>>total_marks;
			cout<<"Enter the obtained marks ="<<endl;
			cin>>Subject_marks;
			 percentage =(Subject_marks*100)/total_marks;
			if(percentage>90)
			{
				cout<<"The grade is A+ and gpa is 4"<<endl;
			}
			else if((percentage>80)&&(percentage<90))
			{
				cout<<"The grade is A and gpa is 4"<<endl;
				
			}
			else if ((percentage>70)&(percentage<80))
			{
				cout<<"The grade is B+ and gpa is 3.70"<<endl;
			}
			else if ((percentage>60)&&(percentage<70))
			{
				cout<<"The grade is B and gpa is 3.30"<<endl;
			}
			else if ((percentage>50)&&(percentage<60))
			{
				cout<<"The grade is C+ and gpa is 2.40"<<endl;
			}
			else if((percentage>40)&&(percentage<=50))
			{
				cout<<"The grade is C and gpa is 2"<<endl;
			}
			else
			{
				cout<<"The grade is F and student is fail"<<endl;
			}
			break;
			case 2:
				{
					cout<<"Enter the gpa of subject one"<<endl;
					cin>>subject1;
					cout<<"Enter the credit hours of subject one "<<endl;
					cin>>credithour1;
					cout<<"Enter the gpa of subject two"<<endl;
					cin>>subject2;
					cout<<"Enter the credit hours of subject two "<<endl;
					cin>>credithour2;
					cout<<"Enter the gpa of subject three"<<endl;
					cin>>subject3;
					cout<<"Enter the credit hours of subject three "<<endl;
					cin>>credithour3;
					cout<<"Enter the gpa of subject four"<<endl;
					cin>>subject4;
					cout<<"Enter the credit hours of subject four "<<endl;
					cin>>credithour4;
					cout<<"Enter the gpa of subject five"<<endl;
					cin>>subject5;
					cout<<"Enter the credit hours of subject five "<<endl;
					cin>>credithour5;
					total_Gpa=((subject1*credithour1)+(subject2*credithour2)+(subject3*credithour3)+(subject4*credithour4)+(subject5*credithour5))/(credithour1+credithour2+credithour3+credithour4+credithour5);
				   cout<<"The total gpa of semester is "<<total_Gpa<<endl;
						}
		}
		cout<<"press 1 to continue and other keys to stop";
		cin>>programControl;

	}
	

}
