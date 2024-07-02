# 19Shop
This is my first project during my internship 19. It was not launched during my internship and was more like a learning tool for me. Here you can find only its readme and some screenshots. Source code is provided on demand

## About the project
Basic internal online shop

## Tools
* Frontend: HTML, CSS, jQuery, JavaScript
* Backend: Django

## To-do
* Add Image model to models
* Add photo galery to every product?
* Update category class and add them to products
* Add more order statuses? 
* Add date for when you come to pick up the order?
* Fill/erase empty headers and subheaders
* Set limits on how many products a person can order?
* Improve validators for uploads (check for dimensions)
* Version for small screens (mostly done)
* Cart - change variant size from cart?

## Existing functionality
* Customer view and staff view
* Product: add, update, delete, display all, display one; zoom image
* Cart: add, update quantity in the order, update quantity in the stock (upon ordering), delete from the cart
* Order: display all, display one, manage all, manage one, update order status, delete order (only by staff)
* Filters for some pages, pagination for all tables and index page
* Display stock, update stock quantity
* Mail notification upon creating an order, changing its status, cancelation
* Models: Product, OrderItem, Order, Variant, Size, Color
* Manager can add color, size, product, variants, manage orders and stock
* CSS for small screens (768 px and less)

## Models:
* ***Category*** - product category, currently not in use
* ***Product*** - product itself; contains only name, description and a general image
* ***Image*** - product image; currently not in user; was intended to be put in use for photo galery 
* ***Size*** - product size
* ***Color*** - product color; i tried to make color options in select to disply the proper color, but my solution did not work; probably, you can find it
* ***Variant*** - product variant; if image is none, it uses img from product
* ***Order*** - order itself; contains general info
* ***OrderItem*** - product variant from the order

## Notes:
* The project has a functional view style
* So far there is a validation for img size. File extension is checked by Pillow. However, for some reasons validation error is not displayd. I tried several solutions, but without much success. Currently if there is an error, the form is simply reset
* Cart is stored in the cache (i think this is more convenient than storing this kind of data in the db)
* Stock is updated only upon order creation. Initially stock was updated upon adding an item to cart, but that solution had several serious flows (for example, it was easy to empty the whole stock)
* To run hub-app-1: docker exec -it hub-app-1 bash 
* To install Pillow execute inside the hub-app-1: python3 -m pip install Pillow
* Initially, I had used bootstrap classes, but then I decided to create custom classes instead (less dependant on bootstrap; classes fields in html look better like this; plus this is a good way to learn better css). In some places I still use bootstrap (navbar)

## Sources:
* tuto: https://www.youtube.com/playlist?list=PLCC34OHNcOtpRfBYk-8y0GMO4i1p1zn50
* homepage and style.css templates: https://startbootstrap.com/template/shop-homepage
* svg icons: https://icon-sets.iconify.design/
* pagination: https://realpython.com/django-pagination/
* pagination + filters (conflict resolution): https://www.youtube.com/watch?v=dkJ3uqkdCcY
* java script for sorting a table: https://www.w3schools.com/howto/howto_js_sort_table.asp
* bootstrap templates: https://getbootstrap.com/docs/5.0/getting-started/introduction/
* scripts for add/delete forms inside formset: https://medium.com/all-about-django/adding-forms-dynamically-to-a-django-formset-375f1090c2b0
* flashlight effect: https://stackoverflow.com/questions/19213652/how-to-give-the-webpage-a-light-in-the-darkness-effect-using-mouse-cursor

## Screenshots
Main page with all the products:
![Main page](https://github.com/baltsaros/19shop/blob/main/pics/main.jpeg)
Version for small screens:
![Small](https://github.com/baltsaros/19shop/blob/main/pics/mobile.jpeg)
Product page before selection:
![Product page 1](https://github.com/baltsaros/19shop/blob/main/pics/product_page.jpeg)
Product page after size and color selection:
![Product page 2](https://github.com/baltsaros/19shop/blob/main/pics/product_page2.jpeg)
Product page after selection a variant with a different image:
![Product page 3](https://github.com/baltsaros/19shop/blob/main/pics/product_page3.jpeg)
Notifications:
![Messages](https://github.com/baltsaros/19shop/blob/main/pics/message.jpeg)
Cart:
![Cart](https://github.com/baltsaros/19shop/blob/main/pics/cart.jpeg)
User orders:
![User Orders](https://github.com/baltsaros/19shop/blob/main/pics/user_orders.jpeg)
Order details:
![Order details](https://github.com/baltsaros/19shop/blob/main/pics/order_details.jpeg)
Form examples:
![Form 1](https://github.com/baltsaros/19shop/blob/main/pics/add_product.jpeg)
![Form 2](https://github.com/baltsaros/19shop/blob/main/pics/size_form.jpeg)
Order management:
![Manage orders](https://github.com/baltsaros/19shop/blob/main/pics/manage_orders.jpeg)
Stock management:
![Manage stock](https://github.com/baltsaros/19shop/blob/main/pics/manage_stock.jpeg)