#include <iostream>
#include <vector>
#include <string>

using namespace std;

struct Book {
    string title;
    string author;
    string division;
};

void searchBook(const vector<Book>& books, const string& keyword) {
    bool found = false;
    cout << "Searching for books containing: " << keyword << endl;
    for (const auto& book : books) {
        if (book.title.find(keyword) != string::npos || book.author.find(keyword) != string::npos) {
            cout << "Title: " << book.title << ", Author: " << book.author << ", Division: " << book.division << endl;
            found = true;
        }
    }
    if (!found) {
        cout << "No books found matching the keyword.\n";
    }
}

int main() {
    vector<Book> library = {
        {"C++ Programming", "Bjarne Stroustrup", "Computer Science"},
        {"Data Structures", "Mark Weiss", "Computer Science"},
        {"History of India", "Romila Thapar", "History"},
        {"Physics Fundamentals", "Richard Feynman", "Science"},
        {"Modern Art", "Pablo Picasso", "Arts"}
    };

    string keyword;
    cout << "Enter book title or author to search: ";
    getline(cin, keyword);

    searchBook(library, keyword);

    return 0;
}
