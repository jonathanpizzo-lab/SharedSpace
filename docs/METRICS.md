[Heart Framework](https://docs.google.com/presentation/d/1I9r6ojzF3B7I_GaOSphr8asDhemSHDfkq52hNfg3dMQ/edit?usp=sharing)

## Metric Collection

- **Login Button CTR** — tracked with two custom Firebase Analytics events: `login_button_tapped` fires every time a user taps "Sign In to My Home", and `login_success` fires when the sign in works. Login success rate = `login_success` ÷ `login_button_tapped`, which shows how many users make it through login and where people drop off.

- **Profile Completion Rate** — We will use Firebase Analytics to track when users open the profile creation page and when they finish creating their profile. We will use the `screen_view` event and a custom event called `profile_completed`. This will help us see how many users complete their profiles instead of leaving the page or skipping it.

- **Household Agreement Acceptance Rate** — We will store each agreement’s ID, version, and the user IDs of household members who accept it in Firestore. When a user selects “Agree,” we will record their acknowledgment and a timestamp. We will calculate the percentage of current household members who have accepted the latest version of each agreement to identify agreements still awaiting responses.

- **User Group Chat** - We will check to see (through firebase analytics) that for each user/ID in a household has contributed to the group chat at least once, acknowledging them as "active" for communication.
