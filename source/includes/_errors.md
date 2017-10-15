# Errors

<aside class="notice">
This is error handling
</aside>

The OpenTrip Api uses the following error codes by response code:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The kitten requested is hidden for administrators only
404 | Not Found -- The specified kitten could not be found
405 | Method Not Allowed -- You tried to access a kitten with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The kitten requested has been removed from our servers
418 | I'm a teapot
429 | Too Many Requests -- You're requesting too many kittens! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.




The OpenTrip Api also uses the following error codes :

<code>
{
  "error": true,
  "code": "PASSWORD_NOT_MATCH"
}
</code>

Error Code | Meaning
---------- | -------
INVALID_EMAIL_ADDRESS | Bad Request -- Your email address is sucks
INVALID_KEY | Not Found -- Your key no found
INVALID_TOKEN | Bad Request -- Your token is sucks
INVALID_TIMESTAMP | Bad Request -- Your timestamps is sucks
INVALID_GENDER | Bad Request -- Your gender is sucks
INVALID_PHONE_NUMBER | Bad Request -- Your phone number is sucks
INVALID_DATE_TRIP | aha -- tanggal trip sama(start&end) atau tanggal tidak lebih dari 6 hari dari tanggal hari itu
PASSWORD_TOO_SHORT | Bad Request -- Your password to short
EMAIL_ADDRESS_NOT_REGISTERED | Not Found -- Email address not registered
PASSWORD_NOT_MATCH | Bad Request -- Wrong password
EMAIL_ALREADY_USE | Bad Request -- Email address already registered
PHONE_NUMBER_ALREADY_USE | Bad Request -- Phone Number already registered
PHONE_NUMBER_ALREADY_VERIFIED | Bad Request -- Phone Number already verified
ID_INSTAGRAM_ALREADY_USE | Baf Request -- Instagram id already registered
USERNAME_INSTAGRAM_ALREADY_USE | Bad Request -- Username alredy registered
ACCESS_TOKEN_REQUIRED | Bad Request -- Need access_token
REFRESH_TOKEN_REQUIRED | Bad Request -- Need refresh_token
INTEREST_ARRAY_REQUIRED | Bad Request -- array cuy
ALREADY_EXISTS | sudah ada
NOT_FOUND | not found
USER_NOT_FOUND | Not Found -- user not registered
USER_NOT_VERIFIED | User account not verified,
ACCOUNT_SUSPENDED | User account was suspended
PARAMETER_REQUIRED | Bad Request -- Need required parameter
PARAMETER_WRONG | Bad Request -- Need required parameter
UNKNOWN_ERROR | Error -- unexpected error
SOCIAL_USER_BLOCKED | Bad Request -- user is blocked
SOCIAL_CANNOT_FOLLOW_YOURSELF | Bad Request -- don't follow yourself
SOCIAL_CANNOT_UNFOLLOW_YOURSELF | Bad Request -- cannot unfollow yourself
SOCIAL_CANNOT_BLOCK_YOURSELF | Bad Request -- You can't block yout self
SOCIAL_CANNOT_UNBLOCK_YOURSELF | Bad Request -- Also cannot unblock yourself



