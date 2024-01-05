# Minimum-Repetitions

#include <iostream>
#include <string>

using namespace std;

int minRepetitions(string A, string B) {
    int lenA = A.length();
    int lenB = B.length();
    
    int repetitions = 0;
    string concatStr = "";

    while (concatStr.length() < 2 * lenB) {
        concatStr += A;
        repetitions++;

        if (concatStr.find(B) != string::npos) {
            return repetitions;
        }
    }

    return -1;
}

int main() {
   
    string A, B;
    cin >> A >> B;

    int result = minRepetitions(A, B);
    cout << result << endl;

    return 0;
}
