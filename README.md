
# Blacket
![Frame 2](https://github.com/madTicket/.github/assets/155048081/4efd430f-162b-4215-bf14-cc5f4d69b553)

## Introduction

Online Musical & Concert Safe Trading AI Platform

## Development Environment

- Frontend: React
- Backend: Flask
- Database: MongoDB ATLAS

## Team Members

- 송지효 - KAIST Computer Science, Class of 2021
- 양준원 - KAIST Industrial Engineering, Class of 2022

## Key Features

### Registration & Login
![Untitled (2)](https://github.com/madTicket/.github/assets/155048081/231a4a09-d9c3-49ad-8b08-c21591e0ee56)
![Untitled (3)](https://github.com/madTicket/.github/assets/155048081/893905a5-421d-4a94-a9cd-32ebb1362056)

- Register and login functionalities on the main page
  - Log in by clicking the login button
  - If not registered, click the sign-up button to register
  - Upon successful login, the login button changes to logout



### Main Page
![Untitled (6)](https://github.com/madTicket/.github/assets/155048081/454619f0-598f-4da7-9985-3b49000ecbe8)

- Search for desired musicals or concerts
  - In-house API DB search functionality
  - Continuously display search results for quick access
  - Click 'View All' to display all registered concerts & musicals information


### Show Detail Page
![Untitled (5)](https://github.com/madTicket/.github/assets/155048081/b0d66b02-1545-49b9-be87-e62c9d601ae7)

- Display detailed information of selected musical & purchase tickets
  - Show detailed information like price, location, and date of the musical
  - Display ticket information
  - Features like cart and wishlist


### Ticket Upload Page
![Untitled (7)](https://github.com/madTicket/.github/assets/155048081/7d4f56be-94c3-4523-81e5-570529ca8e86)
![Untitled (8)](https://github.com/madTicket/.github/assets/155048081/3a8cbdb8-2e3e-4e0e-892e-b0897c19be6d)
![Untitled (10)](https://github.com/madTicket/.github/assets/155048081/b76e3f03-2ea3-4e4a-96d9-6fa8eb295f2a)
![Untitled (11)](https://github.com/madTicket/.github/assets/155048081/658b131e-b879-418e-a3ec-f2ce348e782e)

- Upload tickets for selected shows
  - **Ticket price recommendation feature (predicting the selling time based on different prices)**
  - **Automatic ticket trade price adjustment notification feature**
  - Fill in details like ticket type, date, deadline, serial number, and price
  

### My Page
![Untitled (13)](https://github.com/madTicket/.github/assets/155048081/26167e14-4616-4ef5-939a-5df6780efe12)
![Untitled (12)](https://github.com/madTicket/.github/assets/155048081/10566014-10f5-41f4-b3b2-244746aaac18)
![Untitled (14)](https://github.com/madTicket/.github/assets/155048081/23a91628-5229-4d04-aa10-1b2dc9617d2e)

- View personal information
  - Check cart & tickets being sold
  - Individual product payment via KakaoPay in the cart
  - Member information modification feature


## Thrifty Service
![Untitled (15)](https://github.com/madTicket/.github/assets/155048081/e6344f99-76f6-493b-acb1-2a1ba1c52796)

- Ticket trade price automatic adjustment agent
  - Generate Truncated Normal Distribution based on the State (current average and variance of ticket prices)
  - Calculate P(sold) using the p-value in the Distribution, and determine the optimal action by searching the Q value with a Utility function
- Predictive service for trading duration based on ticket prices
  - Set the ticket seller and buyer as Poisson Distributions
  - Assume that the buyer always purchases the lowest-priced item and simulate the period until my ticket is sold
  - Return the average result of simulations up to 3 seconds
