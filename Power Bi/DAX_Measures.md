# DAX Measures

This project uses the following DAX measures to calculate key performance indicators (KPIs) for the Power BI dashboard.

## Total Bookings

```DAX
Total Bookings = COUNTROWS(July)
```
## Cancelled Bookings

```DAX
Canceled Bookings = CALCULATE(
    COUNTROWS(July), 
    July[Booking_Status] IN {"Canceled by Customer","Canceled by Driver"}
    )
```
## Cancelled Percentage/ Cancellation Rate
```DAX
Cancelled Percentage =
DIVIDE(
    [Cancelled Bookings],
    [Total Bookings],
    0
)
```
Format: Percentage
