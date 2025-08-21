# pat2-subtask-1.
A repository for Morse code within the README,md file tasks, specifically for subtask 1 project.
#include <iostream>
#include <string>
#include <cctype>
using namespace std;

int main() {
    char dot='.', dash='-';   
    string letters="ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
    string morse[]={
        ".-","-...","-.-.","-..",".","..-.","--.","....","..",
        ".---","-.-",".-..","--","-.","---",".--.","--.-",".-.",
        "...","-","..-","...-",".--","-..-","-.--","--..",
        "-----",".----","..---","...--","....-",".....",
        "-....","--...","---..","----."
    };

    string msg, full="";
    cout<<"Enter a short message: ";
    getline(cin,msg);

    for(char c:msg){
        if(c==' ') continue;
        c=toupper(c);
        size_t pos=letters.find(c);
        if(pos!=string::npos){
            cout<<c<<": "<<morse[pos]<<endl;
            full+=morse[pos]+"   ";
        }
    }

    cout<<"\nFull Morse Code Message:\n"<<full<<endl;
}
