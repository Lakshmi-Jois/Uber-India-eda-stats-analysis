 📘 README -- Uber Bookings India Dataset

 📂 Dataset Overview

This dataset contains 150,000 Uber ride booking records in India. It
provides details about ride requests, booking outcomes, cancellations,
ratings, and payment methods. The dataset can be used for ride-hailing
analysis, customer behavior insights, driver performance evaluation, and
demand--supply optimization.

------------------------------------------------------------------------

 📑 File Information

-   File type: CSV / Excel (depending on source)\
-   Rows: 150,000
-   Columns: 21

------------------------------------------------------------------------

 🏷️ Column Descriptions

  -------------------------------------------------------------------------
  Column Name                           Description
  ------------------------------------- -----------------------------------
  Date                                Date of booking (DD/MM/YYYY or
                                        YYYY-MM-DD format)

  Time                                Time of booking (HH:MM:SS format)

  Booking ID                          Unique identifier for each booking

  Booking Status                      Status of the booking (e.g.,
                                        Completed, Cancelled, Incomplete)

  Customer ID                         Unique identifier for the customer

  Vehicle Type                        Type of Uber vehicle booked (e.g.,
                                        UberGo, Premier, Auto, XL)

  Pickup Location                     Starting location of the ride

  Drop Location                       Destination location of the ride

  Avg VTAT                            Average Vehicle Turnaround Time
                                        (time taken for vehicle to reach
                                        pickup)

  Avg CTAT                            Average Customer Turnaround Time
                                        (time customer takes to start trip
                                        after vehicle arrives)

  Cancelled Rides by Customer         Number of times the customer
                                        cancelled the ride

  Reason for cancelling by Customer   Reason provided by customer for
                                        cancellation

  Cancelled Rides by Driver           Number of times the driver
                                        cancelled the ride

  Driver Cancellation Reason          Reason provided by driver for
                                        cancellation

  Incomplete Rides                    Indicator/Count of rides not
                                        completed (e.g., mid-way
                                        termination)

  Incomplete Rides Reason             Reason why the ride was incomplete

  Booking Value                       Monetary value of the booking (fare
                                        amount)

  Ride Distance                       Distance of the ride (in km or
                                        miles, depending on dataset)

  Driver Ratings                      Customer's rating for the driver
                                        (typically 1--5 scale)

  Customer Rating                     Driver's rating for the customer
                                        (typically 1--5 scale)

  Payment Method                      Payment method used (Cash, UPI,
                                        Card, Wallet, etc.)
  -------------------------------------------------------------------------

------------------------------------------------------------------------

 🔍 Possible Analyses

-   Demand vs Supply: Analyze peak booking hours, high-demand
    routes.
-   Cancellations: Study reasons for cancellations by both customers
    and drivers.
-   Performance Metrics: Correlate driver/customer ratings with ride
    outcomes.
-   Revenue Insights: Explore booking values and ride distances.\
-   Operational Efficiency: Investigate Avg VTAT & Avg CTAT to
    assess waiting times.

------------------------------------------------------------------------

 🛠️ Example Usage (Python)

 python
import pandas as pd

 Load dataset
df = pd.read_csv("uber_bookings_india.csv")

 Quick overview
print(df.head())
print(df.info())

 Check cancellation reasons
cancel_by_customer = df["Reason for cancelling by Customer"].value_counts()
print(cancel_by_customer)

