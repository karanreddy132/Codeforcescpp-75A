# Codeforcescpp-75A
#include <bits/stdc++.h>
using namespace std;

int value(int a) {
	int i = 1;
	while (a / i != 0) {
		if (a % 10 == 0) {
			a /= 10;
		} else if ((a / i) % 10 == 0) {
			a = i*(a / (10 * i)) + a % i;
		}
		else{
      i *= 10;
    }
	}
	return a;
}
int main() {
	int n, m, sum;
	cin >> n;
	cin >> m;
	sum = n + m;
	n = value(n);
	m = value(m);
	sum = value(sum);
	if (n + m == sum)
		cout << "YES";
	else
		cout << "NO";
	return 0;
}
