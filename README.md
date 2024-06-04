# CS50’s Web Programming with Python and JavaScript - Project 2: Commerce

## Project Description
This project involves creating an eBay-like e-commerce auction site using Django. The site allows users to:
- Post auction listings
- Place bids on listings
- Comment on listings
- Add listings to a watchlist

The distribution code includes a Django project named `commerce`, which contains a single app called `auctions`.

## Features

### Models
Your application should have at least three models in addition to the User model:
1. **Auction Listings**: To store details about each auction.
2. **Bids**: To store information about bids placed on listings.
3. **Comments**: To store comments made on auction listings.

### Create Listing
Users can create a new listing with the following details:
- Title
- Description
- Starting bid
- Optional: Image URL
- Optional: Category (e.g., Fashion, Toys, Electronics, Home, etc.)

### Active Listings Page
The default route displays all currently active auction listings, showing:
- Title
- Description
- Current price
- Photo (if available)

### Listing Page
A detailed view of a listing with the following features:
- View listing details including the current price
- Add/remove the item to/from the watchlist (if signed in)
- Place a bid on the item (if signed in)
- Close the auction (if the user created the listing and is signed in)
- Display auction winner information (if applicable and signed in)
- Add comments to the listing (if signed in)
- Display all comments made on the listing

### Watchlist
A page for signed-in users to view all listings they have added to their watchlist, with links to each listing's detailed page.

### Categories
A page displaying all listing categories. Clicking on a category shows all active listings within that category.

### Django Admin Interface
Site administrators can:
- View, add, edit, and delete any listings, comments, and bids through the Django admin interface.

## Setup Instructions

### URL Configuration
- Defined in `auctions/urls.py`
- Predefined routes: default index, `/login`, `/logout`, and `/register`

### Views
- Defined in `auctions/views.py`
- Predefined views: `index`, `login_view`, `logout_view`, and `register`

### Running the Application
1. Start the Django web server:
   ```bash
   python manage.py runserver
   ```
2. Open your browser and visit the site.
3. Register for an account and observe the HTML changes based on the authentication status.

### Modifying HTML Layout
- HTML layout is in `auctions/templates/auctions/layout.html`
- Modify this file to change the layout, especially content wrapped in `user.is_authenticated` checks.

### Defining Models
- Define additional models in `auctions/models.py`
- Run migrations after changes:
  ```bash
  python manage.py makemigrations
  python manage.py migrate
  ```

## Specification Details
To complete the auction site, fulfill these requirements:
1. Implement models for auction listings, bids, and comments.
2. Enable users to create listings with title, description, starting bid, image URL, and category.
3. Show all active listings on the default route.
4. Provide a detailed listing page with features for bidding, commenting, and managing the watchlist.
5. Create a watchlist page for users.
6. Implement category pages for listings.
7. Ensure the Django admin interface can manage listings, comments, and bids.

## Contributing
1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

For more details on the project specifications, visit the [CS50 Network Project](https://cs50.harvard.edu/web/2020/projects/2/commerce/).
