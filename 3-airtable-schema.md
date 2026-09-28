# Airtable Tables to Create

Build these 4 tables in your Airtable base. Field names must match exactly.

## Table: `Rooms`
| Field | Type | Values |
|---|---|---|
| Room Name | Single line text | `$100 room`, `$149 room`, `$249 room`, `$300 room` |
| Nightly Rate | Currency | 100 / 149 / 249 / 300 |
| Max Guests | Number | 2 / 2 / 4 / 4 |
| Active | Checkbox | checked |

## Table: `Bookings`
| Field | Type |
|---|---|
| Booking ID | Auto number |
| Guest Name | Single line text |
| Phone | Phone (E.164, e.g. +15551234567) |
| Check-in | Date |
| Check-out | Date |
| Room | Link → Rooms |
| Guests | Number |
| Status | Single select: `confirmed` / `modified` / `cancelled` |
| Total Price | Currency |

## Table: `BlockedDates`
| Field | Type |
|---|---|
| Date | Date |
| Reason | Single line text |

## Table: `CallLogs`
| Field | Type |
|---|---|
| Call ID | Single line text |
| Tool | Single line text |
| Payload | Long text |
| Success | Checkbox |
| Message | Single line text |
| Created At | Created time |
