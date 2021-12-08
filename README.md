#include <iostream>
#include <string>

std::string check_pass(std::string password)
{
    std::string valid_pass = "qazwsx123";
    std::string error_message;
    if (password == valid_pass) {
        error_message = "OK_Access.";
    }
    else {
        error_message = "Access_denied!";
    }
    return error_message;
}

int main()
{
    std::string user_pass;
    std::cout << "enter_password:";
    getline(std::cin, user_pass);
    std::string error_msg = check_pass(user_pass);
    std::cout << error_msg << std::endl;
    return 0;
}
