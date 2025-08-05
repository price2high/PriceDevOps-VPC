# Appointment Booking API

## Endpoint

`POST /api/book-appointment`

## Request Body

```json
{
  "name": "Client Name",
  "company": "Client Company",
  "email": "client@example.com",
  "date": "2025-08-15",
  "details": "Looking for AWS migration services"
}
```

## Response

```json
{
  "status": "confirmed",
  "message": "Appointment booked!"
}
```

## Storage

Data is stored in `appointments.json` on the EC2 instance.

Can be extended to:
- Amazon RDS
- DynamoDB
- S3 archival

