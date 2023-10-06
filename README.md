# bankproject
This is a mini project for banking sector
#include <iostream>
//#include <string.h>
//#include "xyzbank.h"

using namespace std;

class UserLogin {
	private:
		string userName = "username";
		string userPassword = "password";
	public:
		string userNameInput;
		string userPasswordInput;
		bool loginStatus = false;

//		UserLogin() {
//			
//		}

		void login() {
			cout << "Username: ";
			cin >> userNameInput;
			if(userNameInput == userName) {
				cout << "Password: ";
				cin >> userPasswordInput;
				if(userPasswordInput == userPassword) {
					loginStatus = true;
					cout << "GJ! You've successfully Logged in!";
				}
			}
			if(loginStatus == false) {
				cout << "Try Again!";
				login();
			}
		}
};

int main()
{
	UserLogin aUser;
	aUser.login();
	return 0;
}
