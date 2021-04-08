
## Rentr is a fullstack iOS app made using **SwiftUI** and **Firebase**
Rentr is a P2P marketplace that allows users to securely rent out almost anything, similar to fatllama.com.

#### Demo

https://youtu.be/Z_0V_Vwo9HE Rental process (both ends) demo
https://youtu.be/z-MGnwOSexo Lending process demo

#### Context

##### Posting items
The process for posting items goes as follows:
1. Add the item's details
2. Create an account
3. Attach a bank account
4. Post the listing

##### Renting items
The process for initiating a rental session goes as follows:
1. Select the item
2. Create an account
3. Attach a Credit Card
4. Rent out the item

##### Rental Session protocol:
Renter = Person renting the item
Lender = Person lending out the item
When two renters/lenders are in a transaction, the process goes as follows:
1. Someone requests a time and place to meet up for the lender to give the item to the renter
2. The other party has to accept that request
3. They scan QR codes. This is done to ensure that the renter and lender have actually met up, and can be used in insurance/damage claims if the lender destroys the item.
4. Someone requests a time and place to meet up to return the item 
5. The other party accepts that request
6. They scan QR codes to confirm in our database that the renter returned the item to the lender
7. The lender is paid out on the QR code scan

#### Features and Technologies:
- Written fully in Swift with SwiftUI
- MVVM app architecture
- Backend in Firebase and Node (for plaid and stripe)

- Signup: GoogleSignIn and Firebase Auth
- Add Listing: AVFoundation, Plaid 
- SearchView: Algolia, CoreLocation
- Item Interaction: CoreLocation, Firebase Storage, MapKit, Stripe
- Chats: Firebase Database, Stripe (payouts), AVFoundation, QRCode, LocationPicker


