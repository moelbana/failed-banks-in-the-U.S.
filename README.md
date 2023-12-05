# Failed banks in the U.S. from 2000 to 2023 ــــــ An Analysis.
A Tableau Interactive Dashboard and story featuring the failed banks in the U.S. from 2000 to 2023.

## Interactive Dashboard:

**You can check the dashboard I created using Tableau public from this [LINK](https://public.tableau.com/app/profile/mohamed.elbanna/viz/FailedBanksintheU_S_/Dashboard1)**

**Simplified Tableau [Story](https://public.tableau.com/app/profile/mohamed.elbanna/viz/FailedBanksintheU_S__Story/Story1)**

## Tools & Technologies used:
I have used **DBeaver** for SQL editing, data cleaning, and transformation, with **PostgreSQL** as a database engine. For data visualizations and building interactive dashboards, I have utilized **Tableau Public**.

## GLOSSARY
Before scrolling down, you need to read the following to become familiar with the terms used. **You can also watch this [video](https://www.youtube.com/watch?v=n_O1B_2tAlk)**

**1. What is a failed bank?** 
  * When a bank can't manage obligations, a federal or state agency will shut it down. The Federal Deposit Insurance Corporation, or FDIC, will become the "receiver" of the failed bank. The FDIC will make sure that depositors get their insured deposits.

**2. acquiring institution:** A healthy bank or thrift institution that purchases some or all of the assets and assumes some or all of the liabilities of a failed institution.

**3. What is a Charter and charter class?** 
  - A charter is the legal authorization to conduct business and is granted to a financial institution by federal or state government.
  - The FDIC assigns classification codes indicating an institution's charter type (commercial bank, savings bank, or savings association), its chartering agent (state or federal government), its Federal Reserve membership status (member or nonmember), and its primary federal regulator (state charter institutions are subject to both federal and state supervision).

**4. Charter classes used in this report are:**
  - N: National charter commercial bank supervised by the Office of the Comptroller of the Currency.

  - SM: State charter Fed member commercial bank supervised by the Federal Reserve.

  - NM: State charter Fed nonmember commercial bank supervised by the FDIC.

  - SL: federal and state savings and loans supervised by the Office of Thrift Supervision.

  - SB: State charter savings bank supervised by the FDIC.

  - SI: federal charter savings bank supervised by the FDIC.

**5. What is a transaction?**
  - Transaction is the process of resolving an institution.

**6. Transaction types used in this report:**
  - PA: Purchase and Assumption, where the insured and uninsured deposits, certain other liabilities and a portion of the assets were sold to an acquirer.
    
  - PI: Purchase and Assumption of the insured deposits only.

  - PO & DINB: Payout, where the insurer paid the depositors directly and placed the assets in a liquidating receivership.
    
**7. What is the FDIC insurance amount?**
  - The standard insurance amount is **$250,000** per depositor, per insured bank, for each ownership category.

**8. Open Bank Assistance (OBA):** A resolution method in which an insured bank in danger of failing receives assistance in the form of a direct loan, an assisted merger, or a purchase of assets.

**For more information and context you can check [Failed Banks Help](https://banks.data.fdic.gov/explore/failures/help#INTRODUCTION) & [FDIC: GLOSSARY](https://www.fdic.gov/bank/historical/reshandbook/glossary.pdf)**


## Introduction:
**Since the beginning of the millennium, a total of 586 banks have been approached by the FDIC. Among them, 573 have failed, while only 13 banks have received federal government assistance. In this analysis, I will break down each number to examine what happened with these banks.**

### First: Failed banks:

![Total failed](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/cccd06bf-c77a-4b5b-a4c2-b01691393c90)

***Key Summaries/Statistics:***

**1. The approximate total assets of the 573 failed banks combined amount to $1.2 trillion. The top 4 banks hold around $838 billion in assets.**
  - The largest bank failure was Washington Mutual Bank, with the most assets at **$307** billion back in 2008.
  - The second and third largest failures are FIRST REPUBLIC BANK and SILICON VALLEY BANK, with **$212** billion and **$209** billion in assets, respectively, occurring in 2023.
  - SIGNATURE BANK comes in fourth place with **$110** billion in assets, also happening in 2023.
  
Top 10 banks failures (***Note: Dollar figures are in thousands***):

![Sample data](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/2d5768b8-2853-4914-991b-ad8df099d00b)

**2. Top States for Bank Failures:**

 - Georgia, Florida, Illinois, and California are the states where the most failures occurred.
    
    - Georgia: ***94 Banks***
    
    - Florida: ***76 Banks*** 
    
    - Illinois: ***69 Banks***
    
    - California: ***44 Banks***

Number of failed banks per state:

![Failed per state](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/d7ae2df3-713f-420d-ab5e-2ef1a02a3120)

**3. Geographical Distribution:**

![Map](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/ff5c3973-ad3e-4809-8f93-b7bed0d05486)

**4. Asset Analysis:**

![Relations chart](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/58cecf88-c214-4092-a067-c6a52a94012d)

**5. Bank Liquidations and Acquisitions:**

 - A total of 31 banks have been liquidated, and the depositors were paid out directly by the FDIC. The remaining banks were acquired by other banks and institutions.

    - Number of Banks Liquidated: ***31***

    - Number of Banks Acquired by Other Banks or Institutions: ***542***

Here's the total number of banks acquired by a single bank or institution

![Acquiring Institutions](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/41a2d527-d2ad-4321-a835-0951c09b1e94)

**6. *Stats regarding the charter class and transaction type*:**
  - Charter class:
    - **60%:** State charter, ***fed none-member***, commercial banks.
    - **15%:** National chartered commercial banks.
    - **11%:** State charter savings banks.
    - **10%:** State charter, ***fed member***, commercial bank.
    - **3%:** Federal charter savings bank.
    - **1%:** Federal and state savings and loans banks.

  - Transaction types:
    - **89%:** Banks were assumed by another institution.
    - **6%:** Banks were partially acquired(insured deposits only).
    - **5%:** Banks were shut down and liquidated.

![Charter](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/6427bb2e-f934-48c5-aa03-4a3baf322f88)

![Transaction](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/f751bd55-a892-48f4-bc62-85e32765291f)

### Second: Big Banks that were bailed out (Too big to fail?):

  -	In 2008, ***CITIBANK, National Association***, with approximate total assets of **$1.2** trillion, was on the verge of failure ***during the financial crisis***. It was bailed out through an Open Bank Assistance Program (OBAM) by the federal government.
  -	similarly in 2009, ***Bank of America N.A.***, with approximate total assets of **$1.4** trillion got into the same program.
  -	Surprisingly during the same two years, another 11 banks, with approximate total assets of **$545 billion**, joined the program. However, after that, nine of them were acquired by only ***two big banks mentioned above.***

**Banks acquired by Bank Of America N.A.:**

  1.	FIA Card Services N.A. ($159 billion in assets).
  2.	Countrywide BANK FSB ($118 billion in assets).
  3.	MERRILL LYNCH BANK USA ($61.9 billion in assets).
  4.	MERRILL LYNCH BANK & TRUST CO FSB ($38 billion in assets).
  5.	Bank Of America Rhode Island N.A. ($35 billion in assets).
  6.	Bank Of America Oregon N.A. ($11.5 billion in assets).

**Banks acquired by CITIBANK, National Association:**
  
  1.	CITIBANK (South Dakota) N.A. ($77.7 billion in assets).
  2.	CITICORP Trust Bank, FSB ($19.6 billion in assets).
  3.	Department Stores National Bank ($375 million in assets)

**The remaining two banks, ***Bank of America California N.A.($21 billion in assets)***, still **maintain operations**. The other, ***CITIBANK(BANAMEX USA), with $1.3 billion in assets***, was closed and liquidated.**

![Capture](https://github.com/moelbana/failed-banks-in-the-U.S./assets/38138546/4c2e6a14-1a55-4958-bae5-1767ea972d36)
