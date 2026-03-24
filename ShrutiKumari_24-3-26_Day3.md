int maxProfit(int* prices, int pricesSize) {
    if (pricesSize == 0) return 0;

    int minPrice = prices[0];
    int maxProfit = 0;

    for (int i = 1; i < pricesSize; i++) {
        if (prices[i] < minPrice) {
            minPrice = prices[i];
        }

        int profit = prices[i] - minPrice;

        if (profit > maxProfit) {
            maxProfit = profit;
        }
    }

    return maxProfit;
}

<img width="1905" height="872" alt="Screenshot 2026-03-24 184449" src="https://github.com/user-attachments/assets/b636ace5-6eba-47bf-8fed-69bc8ab79740" />
