# Pathrose Marine - Mobile App PRD

## Overview
Marine spare parts ordering mobile app for fishermen and boat operators.

## Tech Stack
- **Frontend**: Expo React Native with TypeScript
- **Backend**: FastAPI + MongoDB
- **Auth**: Mock OTP phone authentication (ready for Supabase integration)

## Key Features Implemented

### Authentication
- Phone OTP login (MOCK - shows OTP in alert for testing)
- User signup with name, harbour, language selection
- Admin detection (phone: 7200599700)
- Session persistence with AsyncStorage

### User Features
- Home screen with categories, recommendations
- Voice search button (demo mode)
- Product browsing by category
- Product search with suggestions
- Add to cart functionality
- Wishlist management
- Checkout via WhatsApp or Call
- Profile management

### Admin Features
- Admin dashboard with stats
- View orders
- View users
- Product management (coming soon)

## API Endpoints
- `/api/auth/send-otp` - Send OTP
- `/api/auth/verify-otp` - Verify OTP
- `/api/auth/signup` - Complete signup
- `/api/products` - Get products
- `/api/categories` - Get categories
- `/api/cart/{phone}` - Cart operations
- `/api/orders/{phone}` - Order operations
- `/api/wishlist/{phone}` - Wishlist operations
- `/api/harbours` - Get harbours
- `/api/admin/stats` - Admin statistics

## Test Credentials
- **Admin Phone**: 7200599700
- **Regular User**: Any 10-digit number
- **OTP**: Shown in alert (mock mode)

## Seed Data
Run `POST /api/seed` to populate:
- 8 Categories: Lights, Starter Motor, Battery, Engine Parts, Wiring, Tools, Safety, Pumps
- 19 Products with prices
- 8 Harbours: Chennai, Rameswaram, Tuticorin, Kanyakumari, etc.

## Future Integration
- Supabase Auth (real OTP)
- Voice search with Expo Speech
- Push notifications
- Real payment integration
