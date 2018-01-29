# same
	private static void getBuyOrderPrice(String sellPriceStr) throws ParseException {
		Double sellPrice = NumberFormat.getNumberInstance().parse(sellPriceStr).doubleValue();
		Double limitBuyPrice = sellPrice;
		
		if (sellPrice % 50.00 == 0) {
			limitBuyPrice = sellPrice - 50.00;
		} 
		if (sellPrice % 25.00 == 0) {
			limitBuyPrice = sellPrice - 25.00;
		} 
		if (sellPrice % 10.00 == 0) {
			limitBuyPrice = sellPrice - 10.00;
		} 
		if (sellPrice % 0.50 == 0) {
			limitBuyPrice = sellPrice - 5.00;
		}
	}

	private static void placeBuyOrder(double limitBuyPrice) {
		System.out.println("Placing Buy Order for : " + limitBuyPrice);
		double currentPrice = 1165.00;
		//TODO: SEL
		//TODO: REDUCE TIMESTAMP BETWEEN TEXT BOXES FROM 1000-->100
		if (limitBuyPrice >= currentPrice) {
			//TODO: limitBuyPrice = Round of CurrentPrice - 0.50;
		}
	}

	private static void getSellOrderPrice(String buyPriceStr, int buyIndex) throws ParseException {
		Double buyPrice = NumberFormat.getNumberInstance().parse(buyPriceStr).doubleValue();
		Double limitSellPrice = buyPrice;
		
		if (buyPrice % 50.00 == 0) {
			limitSellPrice = buyPrice + 50.00;
			placeSellOrder(limitSellPrice);
		} 
		if (buyPrice % 25.00 == 0) {
			limitSellPrice = buyPrice + 25.00;
			placeSellOrder(limitSellPrice);
		} 
		if (buyPrice % 10.00 == 0) {
			limitSellPrice = buyPrice + 10.00;
			placeSellOrder(limitSellPrice);
		} 
		if (buyPrice % 0.50 == 0) {
			limitSellPrice = buyPrice + 5.00;
			placeSellOrder(limitSellPrice);
		}
	}
	
	private static void placeSellOrder(double limitSellPrice) {
		System.out.println("Placing Sell Order for : " + limitSellPrice);
		double currentPrice = 1165.00;
		//TODO: SEL
		//TODO: REDUCE TIMESTAMP BETWEEN TEXT BOXES FROM 1000-->100
		if (limitSellPrice <= currentPrice) {
			//TODO: limitSellPrice = Round of CurrentPrice + 1.50;
		}
	}
