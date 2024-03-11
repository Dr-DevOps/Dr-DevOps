# Edit Rate Limiting Rule Documentation

## APIs Covered:
- `/common-services/otp/v2/create`
- `/common-services/validate/v2/email`
- `/common-services/email/send/custom`

## Rate Limiting Configuration:
- **Requests:** 10 requests
- **Period:** 1 minute

## Exceeding Rate Actions:
- **Action:** Block

## Duration of Blocking:
- **Duration:** 1 hour

## Response Type:
- **Default Cloudflare Rate Limiting Response**
- **Response Code:** 429

---

### Usage Instructions:
1. **Log in** to your Cloudflare dashboard.
2. Go to the **Firewall** section.
3. Select **Rate Limiting** from the submenu.
4. Click on **Create a Rate Limiting Rule**.
5. Specify the following details:
   - **Route:** Enter the API route(s) mentioned above.
   - **Requests:** Set to 10.
   - **Period:** Set to 1 minute.
   - **Action:** Choose "Block".
   - **Duration:** Set to 1 hour.
   - **Response Type:** Default Cloudflare rate limiting response with response code 429.
6. Click **Save** to apply the rule.

### Notes:
- This rate limiting rule is designed to mitigate excessive requests to the specified APIs.
- Adjust the parameters as needed to match your specific use case and traffic patterns.
- Monitor the rate limiting logs in your Cloudflare dashboard to ensure the rule is effectively managing traffic.
