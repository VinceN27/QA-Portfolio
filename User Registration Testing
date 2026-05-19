# OpenCart Manual Testing — User Registration

## Testing User Registration on OpenCart Demo Website which mimicks an e-commerce website.

## Test Cases

### RTC_001 — Valid Registration
| Field | Details |
|---|---|
| **Precondition** | Email is not registered |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF, LastName: userL, Email: userFL@gmail.com, Password: useruser) 2. Agree to Privacy Policy 3. Press Continue |
| **Expected Result** | An account will be created |
| **Actual Result** | The account is created and is redirected to a welcome page |
| **Status** | ✅ Pass |

---

### RTC_002 — Invalid Registration: The Same Email
| Field | Details |
|---|---|
| **Precondition** | Email is already registered with an account |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF1, LastName: userL1, Email: userFL@gmail.com, Password: useruser1) 2. Agree to Privacy Policy 3. Press Continue |
| **Expected Result** | Error message stating account is already registered |
| **Actual Result** | A prompt appears stating that the email is already registered |
| **Status** | ✅ Pass |

---

### RTC_003 — Password Validation
| Field | Details |
|---|---|
| **Precondition** | All fields are filled in correctly |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF2, LastName: userL2, Email: userF2@gmail.com, Password: useruser2) 2. Agree to Privacy Policy 3. Press Continue |
| **Expected Result** | A confirm password field should be on the registration page, and an error message should appear for mismatched passwords |
| **Actual Result** | No confirm password/validation field is present hence password validation cannot be performed |
| **Status** | ❌ Fail — See BUG_001 |

---

### RTC_004 — Password Strength
| Field | Details |
|---|---|
| **Precondition** | All fields are filled in correctly |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF2, LastName: userL2, Email: userF2@gmail.com, Password: dogs) 2. Agree to Privacy Policy 3. Press Continue |
| **Expected Result** | Error message stating the password is too weak |
| **Actual Result** | Registration was successful and was redirected to welcome page |
| **Status** | ❌ Fail — See BUG_002 |

---

### RTC_005 — Unchecked Privacy Policy
| Field | Details |
|---|---|
| **Precondition** | All fields are entered correctly |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF2, LastName: userL2, Email: userF2@gmail.com, Password: useruser2) 2. Uncheck agreement to Privacy Policy 3. Press Continue |
| **Expected Result** | Error message stating user must agree to privacy policy |
| **Actual Result** | Error message on the top right screen stating user must agree to privacy policy |
| **Status** | ✅ Pass |

---

### RTC_006 — Empty Required Fields
| Field | Details |
|---|---|
| **Precondition** | All fields are empty |
| **Steps** | 1. Agree to Privacy Policy 2. Press Continue |
| **Expected Result** | Error message stating fields can't be blank |
| **Actual Result** | All required empty field input box turned red, prompting the user that they're required and showing correct input formats |
| **Status** | ✅ Pass |

---

### RTC_007 — Invalid Email Format
| Field | Details |
|---|---|
| **Precondition** | All fields except email are filled and in the right format |
| **Steps** | 1. Fill in all the fields correctly in the right format (FirstName: userF2, LastName: userL2, Email: userF2gmail.com [wrong format], Password: useruser2) 2. Check agreement to Privacy Policy 3. Press Continue |
| **Expected Result** | Error message showing email is not in the correct format |
| **Actual Result** | The prompt shows the user the correct format of an email |
| **Status** | ✅ Pass |

---

## Bug Reports

### BUG_001 — No Password Validation/Confirmation
| Field | Details |
|---|---|
| **Description** | The website allows user registration without password validation |
| **Precondition** | The user must be on the registration page |
| **Steps to Reproduce** | Looking at the registration page, there is no input box for password validation or password confirmation |
| **Expected Result** | A separate textbox with its own separate heading prompting user to confirm the password |
| **Actual Result** | The heading and textbox are missing |
| **Severity** | 🔴 High |

---

### BUG_002 — Password Weakness/Strength Validation
| Field | Details |
|---|---|
| **Description** | The website allows user registration with weak password |
| **Precondition** | The user must be on the registration page |
| **Steps to Reproduce** | 1. Fill in all the fields correctly in the right format (FirstName: userF3, LastName: userL3, Email: userF3@gmail.com, Password: dogs) 2. Check agreement to Privacy Policy 3. Press Continue |
| **Expected Result** | Error message stating the password is too weak |
| **Actual Result** | Registration was successful with a common word, only containing 4 characters |
| **Severity** | 🔴 High |
