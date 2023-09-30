# CASE STUDY #2 - PIZZA RUNNER
## General information
**Case study source:** [Case Study #2 - Pizza Runner](https://8weeksqlchallenge.com/case-study-2/)

**Dataset:** [Here]() you can find script with dataset and table creation process using SQLite.

**Problem:** Danny was scrolling through his Instagram feed when something really caught his eye - “80s Retro Styling and Pizza Is The Future!”. He has prepared for us an entity relationship diagram of his database design but requires further assistance to clean his data and apply some basic calculations so he can better direct his runners and optimise Pizza Runner’s operations. 

**Entity relationship diagram:**
```mermaid
erDiagram
    RUNNERS {
        String runner_id 
        Date registration_date
    }

    CUSTOMER_ORDERS {
        Int order_id
        Int pizza_id
	      String exclusions
        String extras
        Date order_date
    }

    RUNNER_ORDERS {
        Int order_id
        Int runner_id
        String pickup_time
        String distance
        String duration
        String cancellation
    }

    PIZZA_RECIPES {
        Int pizza_id
        Text toppings
    }

    PIZZA_TOPPINGS {
        Int topping_id
        Text topping_name
    }
    
    PIZZA_NAMES {
        Int pizza_id
        Text pizza_name
    }

RUNNER_ORDERS ||--|{ CUSTOMER_ORDERS : relate
RUNNERS ||--|{ RUNNER_ORDERS : do
PIZZA_NAMES ||--|{ CUSTOMER_ORDERS : in
PIZZA_RECIPES ||--|{ CUSTOMER_ORDERS : in
```
## A. Pizza metrics
## Questions and Solutions
### 1. 