import java.util.*;

class Stock {
    String ticker;
    double price;

    Stock(String ticker, double price) {
        this.ticker = ticker;
        this.price = price;
    }
}

class PortfolioItem {
    String ticker;
    int quantity;
    double avgBuyPrice;

    PortfolioItem(String ticker, int quantity, double avgBuyPrice) {
        this.ticker = ticker;
        this.quantity = quantity;
        this.avgBuyPrice = avgBuyPrice;
    }
}

public class StockTradingSimulator {
    static Scanner scanner = new Scanner(System.in);
    static Map<String, Stock> market = new HashMap<>();
    static Map<String, PortfolioItem> portfolio = new HashMap<>();
    static double cashBalance = 100000;

    public static void main(String[] args) {
        // Initialize Market Data
        market.put("AAPL", new Stock("AAPL", 172.5));
        market.put("GOOGL", new Stock("GOOGL", 2820.0));
        market.put("TSLA", new Stock("TSLA", 720.0));
        market.put("MSFT", new Stock("MSFT", 310.0));

        while (true) {
            System.out.println("\n=== Stock Trading Simulator ===");
            System.out.println("1. View Market");
            System.out.println("2. Exit");
            System.out.print("Choose an option: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    viewMarket();
                    break;
                case 2:
                    System.out.println("Exiting. Goodbye!");
                    return;
                default:
                    System.out.println("Invalid choice. Try again.");
            }
        }
    }

    static void viewMarket() {
        System.out.println("\n--- Market Data ---");
        for (Stock stock : market.values()) {
            System.out.printf("%s: $%.2f%n", stock.ticker, stock.price);
        }
    }
}
