# SwissBorg Business data analyst tech challenge

The Swissborg app allows users to easily buy and trade cryptos. They can make fiat or crypto
deposits and withdrawals, trade between any two currencies directly, earn additional yield on
some tokens, or purchase complex investment products such as automatically rebalanced
thematic bundles.

## A. Case study

Recently we launched a new product, the golden thematic. In this tech challenge we ask you to
step into the role of a data analyst collaborating with the product manager responsible for the
release.

We will provide the following two datasets that you can use
user_list table download here:

Containing one row per user with information around onboarding. The table contains records
only on users who started the onboarding during 2023 H1.

- User_id: unique identifier of user
- country_code: country of residence of the user, given during registration
- phone_registered_at: the time the user first registered their phone number in the
SwissBorg app, this is the first step of the onboarding process.
- verified_at: timestamp when user’s identity verification was first approved. After this point
they can access all features within the app (deposits, trading, purchasing investment
products)
- first_deposit_timestamp: the time the user first transferred any funds to the SwissBorg
app.
- Total_claimed_wealth_usd: categorical, Self-declared total wealth of the user
- Current age of the user


Daily aggregates of deposits, withdrawals, spot trade volumes (simple trading between different
currencies available in the app), and purchase or selling of thematic products (web3 or golden
thematics). This table also only contains data for users who started the onboarding process
during 2023 H1.

### Tasks:

I. Two weeks before the public release of the golden thematic, the responsible product
manager reaches out to ask for an assessment on what they can expect in terms of
adoption for this new product. Propose a set of metrics that you believe to be relevant,
and create a business report that you could present to the product manager and the
executive team that evaluates the possible business impact of the new feature. How
would you define pessimistic/realistic/optimistic targets for the most relevant proposed
metrics?
II. During your initial discussion the product manager mentions several times that some
user segmentation would be great, but they don’t have any clear ideas in mind. Take this
into account during your exploration and in your presentation.
III. A week after the launch of the new golden thematic, the product manager comes back to
you asking to evaluate the success of the release, as he finds it somewhat
underwhelming. He also asks what can be done to increase adoption, and once again
mentions a cohort analysis to identify better/worse performing user groups. Can you find
any patterns that could help improve overall adoption? If yes, what actions can you
propose? What (if any) additional support would you need to deliver on those?

## B. SQL challenges:

Considering the above datasets, create sql queries according to the following specifications:

1. Write a query that gives the number of users passing each step of the activation funnel
(installation - verification - deposit - purchase of any thematic bundle), broken down per
country, with conversion rates between each step as well as the overall conversion rate
from the start of the user funnel.
2. Write a query that returns a daily time series of the 14-day rolling net deposit-withdrawal
amount per country for 2023 H1.
3. Write a query and create a corresponding chart that you believe the best highlights the
similarities or differences of the distribution of investment amounts into the web3 and
golden thematics.

## Deliveries:

Please provide the scripts/notebook of your analysis, and create a presentation summarizing
your findings and recommendations that you could present to stakeholders (product/marketing
managers).
For the questions about the SQL queries, please provide the queries and also create a plot
where it is asked. Optional tip: Feel free to use the pandasql library to test the queries (not
required, fully up to you if you find it useful.)
Good luck!