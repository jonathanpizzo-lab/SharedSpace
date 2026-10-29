# A/B Testing

## One-Screen vs Two-Screen Login and Sign Up

**A/B Test Name:** One-Screen vs Two-Screen Login/Sign Up

**User Story Number:** US1

**Metrics:** Adoption, login button CTR, Retention

**Hypothesis:** Having login and sign up on the same screen with tabs is less confusing than making users navigate between two separate screens. We think users are more likely to finish creating an account if both options are visible right away. We expect the single screen version to have a higher signup completion rate.

**Problem:** Users might be dropping off before finishing account creation. We want to figure out if the layout of the login and signup screens is making that worse.

**Experiment:** We'd use Firebase Remote Config with a variable called `single_screen_auth` to control which version a user sees. New users would be randomly split 50/50. Firebase Analytics would track `login_button_tapped` and `signup_button_tapped` events to measure how many people actually complete the flow. We'd run it for at least two weeks.

**Variations:**

Variant A (Control) - the current design with login and sign up on one screen using tabs

Variant B (Test) - login and sign up on two separate screens with a link to switch between them


##Profile Creation Layout Test

**A/B Test Name:** Full Profile Form vs Simplified Profile Form

**User Story Number:** US3

**Metrics:** Adoption, Engagement, Task Success

**Hypothesis:** We believe that keeping the profile creation page simple will encourage more users to complete their profiles. Giving users the option to add extra details later could make the process easier.

**Problem:** Some users may skip setting up their profile because there is too much information to fill out. We want to see if reducing the number of visible fields helps users finish their profiles.

**Experiment:** We will use Firebase Remote Config to display two different profile layouts to new users. Each version will be shown to 50% of users. Firebase Analytics will record when users open the page, complete their profile, or skip it. After two weeks, we will compare the results.

**Variations:**

Variant A (Control) - Users see all the profile fields on the page and can fill them out before continuing.

Variant B (Test) - Users see only the required fields at first and can expand a section to add more information if they want.
