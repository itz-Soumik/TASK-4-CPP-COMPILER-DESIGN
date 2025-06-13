#include <iostream>
#include <stack>
#include <string>
using namespace std;

int operate(int left, int right, char op) {
    switch (op) {
        case '+': return left + right;
        case '-': return left - right;
        case '*': return left * right;
        case '/': return right != 0 ? left / right : 0;
        default: return 0;
    }
}

int precedence(char op) {
    if (op == '+' || op == '-') return 1;
    if (op == '*' || op == '/') return 2;
    return 0;
}

int parse_Evaluate(string exp) {
    stack<int> nums;
    stack<char> ops;
    int i = 0;
    while (i < exp.size()) {
        if (isspace(exp[i])) {
            i++;
            continue;
        }
        if (isdigit(exp[i])) {
            int num = 0;
            while (i < exp.size() && isdigit(exp[i])) {
                num = num * 10 + (exp[i] - '0');
                i++;
            }
            nums.push(num);
            continue;
        }
        if (exp[i] == '+' || exp[i] == '-' || exp[i] == '*' || exp[i] == '/') {
            while (!ops.empty() && precedence(ops.top()) >= precedence(exp[i])) {
                int right = nums.top(); nums.pop();
                int left = nums.top(); nums.pop();
                char op = ops.top(); ops.pop();
                nums.push(operate(left, right, op));
            }
            ops.push(exp[i]);
        }
        i++;
    }

    while (!ops.empty()) {
        int right = nums.top(); nums.pop();
        int left = nums.top(); nums.pop();
        char op = ops.top(); ops.pop();
        nums.push(operate(left, right, op));
    }

    return nums.top();
}

int main() {
    string expression;
    cout << "Enter Expression: ";
    getline(cin, expression);
    cout << "Result: " << parse_Evaluate(expression) << endl;
    return 0;
}
