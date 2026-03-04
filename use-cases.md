# Use Case: Publish Product

## 1. Use Case Name
Publish Product to Marketplace

## 2. Actor
Seller

## 3. Description
Allows seller to create and publish a product listing in the marketplace showcase.

## 4. Preconditions
- Seller is registered
- Seller is logged into personal account
- Seller account is verified

## 5. Main Flow (Basic Scenario)

1. Seller logs into personal account.
2. Seller clicks "Add Product".
3. System displays product creation form.
4. Seller enters product details:
   - Title
   - Description
   - Price
   - Category
   - Images
5. Seller clicks "Submit".
6. System validates fields.
7. System saves product.
8. Product is published (or sent for moderation).

## 6. Alternative Flows

A1: Missing required fields  
→ System shows validation error.

A2: Image upload fails  
→ System shows upload error.

A3: Product requires moderation  
→ Product status set to "Pending Approval".

## 7. Postconditions
- Product is available in marketplace
OR
- Product is saved in pending status
