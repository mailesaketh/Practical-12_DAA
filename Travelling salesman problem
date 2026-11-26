#include <iostream>
using namespace std;

int main()
{
    int n, cost[10][10], visited[10] = {0};
    int totalCost = 0, current = 0;

    cout << "Enter number of cities: ";
    cin >> n;

    cout << "Enter cost matrix:\n";

    for(int i = 0; i < n; i++)
    {
        for(int j = 0; j < n; j++)
        {
            cin >> cost[i][j];
        }
    }

    visited[0] = 1;

    cout << "Path: 1 ";

    for(int i = 1; i < n; i++)
    {
        int minCost = 9999, next = -1;

        for(int j = 0; j < n; j++)
        {
            if(!visited[j] && cost[current][j] < minCost)
            {
                minCost = cost[current][j];
                next = j;
            }
        }

        current = next;
        visited[current] = 1;
        totalCost += minCost;

        cout << current + 1 << " ";
    }

    totalCost += cost[current][0];

    cout << "1";
    cout << "\nMinimum cost: " << totalCost;

    return 0;
}
