# Little Basket

A grocery list planner that writes your shopping list for you, styled like a picnic.

**Try it:** https://anugrahasn1.github.io/little-basket/

First you fill in one page of preferences: what you're shopping for, who's eating, your budget and any food needs. Then "Write my list" takes you to the finished list, and "Change my answers" takes you back.

- **The week:** a balanced shop across fruit and veg, protein, dairy, carbs, cupboard basics, snacks and drinks
- **A picnic:** only things you can eat outdoors without cooking (bread, cheese, fruit, deli, snacks, drinks)
- **Dinner:** three meal ideas with the ingredients and what they cost

It handles vegetarian, vegan, pescatarian, gluten-free, dairy-free, nut-free, no pork and high protein, plus a "leave out" box for anything you don't like. You can tick items off as you shop, make the list cheaper, shuffle it for different products, and copy it to paste into your notes.

## How it builds the list

1. Filters the products by your food needs and the things you want to leave out
2. Splits the budget across food groups (for example about 20% fruit and veg, 17% meat and fish for a weekly shop)
3. Fills each group, rotating between types of product so you don't get five kinds of pasta
4. Scales the amounts to the number of people and days
5. Spends what's left on the groups that got the least

Dinner ideas pick the cheapest matching protein, carb and vegetable for each recipe, assuming one pack feeds about two people.

## Where it came from

This started as a chat assistant I built in Python for one supermarket's product list. I turned the logic into a general planner that runs in any browser, with the products translated into English and the store branding removed. `build_catalogue.py` does that conversion.

## Limits

- Prices come from a sample supermarket price list, so they're examples. Your shop will differ.
- Allergy filters work on product names. Always check the label.
- The catalogue has about 190 products, so lists stick to everyday basics.

## Files

- `index.html` – the whole app (HTML, CSS and JavaScript, no install needed)
- `catalogue.json` – the product list it uses
- `build_catalogue.py` – turns the original store file into the generic catalogue
