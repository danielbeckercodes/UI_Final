Real Estate Listings Web Application (group51-proj1-3)

Our database is hosted under the PostgreSQL account: user: db3842, password: group51
(This is the same database that we used for part 2 of the project) 
The External IP address for the VM is: 35.237.180.188

Web Application URL
When our virtual machine is running, our application is accessible at: http://35.237.180.188:8111/

Description of Implementation vs. Proposal
Our original proposal planned a real estate web platform that supported 
- Relevant buyer interation in realtion to sellers and realtors
- Properties: There are property details for all listings.
- Listings: Properties that can be viewed and searched
- Saved Listings: Buyers can save listings
- Transactions: Displays closed deals by buyers and sellers
- Reviews: Users can review properties

Implemented from Proposal
- Buyers were implemented and handled during log in. This login ensures that only the logged in individuals saved listings are displayed.
- Display of real estate listings with dynamic search and filter functionality
- Buyers are able to save listings
- Transaction and review history is accessible
- Session based login: A user can log in and can see all listings and only their saved listings related to their userID
- One 

Minor devation from proposal 
- Finding trends to identify hot market. We dont have enough data or the data science background to create this algorithm. We were not able to
  make a recommndation algorithm to suit the users' preferences.
- We decided for reviews that it made more sense for the users to review the property instead of the realtors so we focused on reviews for the properties. This is consistent with out part2 database and schema. 


Pages with Notable Database Operations
1) Saved Listings (/saved_listings)
   - Queries the saved_listings table, filtering by the buyer_id stored in query arguments, from the user login.
   - Displays listings saved by the currecntly logged-in user.
   - Button logic dynamically changes from "Saved listing" to "Saved" based on whether the record exists in our database.
   - These live updates are observable in both the home and in the listing/[property_id]/[user_id]
   - Query involves a JOIN between saved_listings, listings, and properties tables to correcly display the saved listings.
  
2) Add Listing (/add_listing)
   - Allows any logged-in user to add a listing for other users to see. 
   - The form asks the user to submit details like a title, location, proprety type, square footage, and price, amongst other relevant
     information.
   - The after the information has been filled out, the listing will be added to our database, where it will now be available in our website
     to see. 
  



# UI_Final
# UI_Final
