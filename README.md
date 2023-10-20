def vendingMachine(items_data, run, item):
   while run:
      buyItem = int(
         input("\n\nEnter the item code for the item you want to buy: "))
      if buyItem < len(items_data):
         item.append(items_data[buyItem])
      else:
         print("THE PRODUCT ID IS WRONG!")
      moreItems = str(
         input("type any key to add more things, and type q to stop:  "))
      if moreItems == "q":
         run = False
   receiptValue = int(
      input(("1. Print the bill? 2. Only print the total sum: ")))
   if receiptValue == 1:
      print(createReceipt(item, reciept))
   elif receiptValue == 2:
      print(sumItem(item))
   else:
      print("INVALID")
