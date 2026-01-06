print('<<<<<<< VENDING MACHINE >>>>>>>')
items = {
    1: {'name': 'zoi ice tea berry', 'price': 4.0, 'stock': 10},
    2: {'name': 'zoi ice tea mango', 'price': 4.0, 'stock': 10},
    3: {'name': 'zoi ice tea strawberry kiwi', 'price': 4.0, 'stock': 10},
    4: {'name': 'zoi ice tea peach', 'price': 4.0, 'stock': 10},
    5: {'name': 'zoi ice tea lemon & mint', 'price': 4.0, 'stock': 10},
    6: {'name': 'zoi ice tea tropical', 'price': 4.0, 'stock': 10},
    7: {'name': 'pepsi', 'price': 3.25, 'stock': 10},
    8: {'name': 'mirinda orange', 'price': 3.25, 'stock': 10},
    9: {'name': 'mountain dew', 'price': 3.25, 'stock': 10},
    10: {'name': '7 up', 'price': 3.25, 'stock': 10},
    11: {'name': 'root beer', 'price': 3.25, 'stock': 10},
    12: {'name': 'sprite', 'price': 3.25, 'stock': 10},
    13: {'name': 'mirinda citrus', 'price': 3.25, 'stock': 10},
    14: {'name': 'coca cola', 'price': 3.25, 'stock': 10},
    15: {'name': 'chocolate cookies', 'price': 4.0, 'stock': 10},
    16: {'name': 'Doritos', 'price': 2.50, 'stock': 10},
    17: {'name': 'Lays', 'price': 2.50, 'stock': 10},
    18: {'name': 'M&Ms', 'price': 2.50, 'stock': 10},
    19: {'name': 'KitKat', 'price': 2.50, 'stock': 10},
    20: {'name': 'Maltesers', 'price': 2.50, 'stock': 10},
}

while True:
    print('\n ----- ITEMS -----')
    for key, item in items.items():
        print(f"{key}. {item['name']} - SAR{item['price']} (stock: {item ['stock']})")

    print('0. Exit')

    choice = int(input('\nEnter item number: '))
    if choice == 0:
        break
    if choice in items:
        selected = items[choice]

        if selected['stock'] == 0:
            print('No more stocks')
            continue

        quantity = int(input('Enter quantity: '))

        if quantity > selected['stock']:
            print('Not enough stock available.')
            continue
        total_cost = selected['price'] * quantity
        print(f'Totak cost: SAR{total_cost}')

        money = float(input('Insert money: SAR'))
        if money >= total_cost:
            selected['stock'] -= quantity
            change = money - total_cost

            print('\nYOUR RECEIPT')
            print(f'Item: {selected['name']}')
            print(f'Quantity: {quantity}')
            print(f'Total Paid: SAR{total_cost}')
            print(f'Change: SAR{change: .2f}')
        else:
            print('Not enough money. Transaction canceled.')
    else:
        print('Invalid selection.')

    again = input('\nWould you like to buy another item? (yes/no): ').lower()
    if again != 'yes':
        break
print('\nThank you for using the vendibng machine!')
