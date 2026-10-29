[Heart Framework](https://docs.google.com/presentation/d/1I9r6ojzF3B7I_GaOSphr8asDhemSHDfkq52hNfg3dMQ/edit?usp=sharing)

## Metric Collection

- **Login Button CTR** — tracked using a custom Firebase Analytics event called `login_button_tapped` that fires when a user taps "Sign In to My Home". We log whether the attempt was successful or not, which helps us see how many users are making it through login and where people might be dropping off.

- **Profile Completion Rate** — We will use Firebase Analytics to track when users open the profile creation page and when they finish creating their profile. We will use the `screen_view` event and a custom event called `profile_completed`. This will help us see how many users complete their profiles instead of leaving the page or skipping it.
