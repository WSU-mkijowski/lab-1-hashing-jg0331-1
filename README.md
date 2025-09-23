[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SLc4hyUA)
# Lab 1 : CEG 3400 Intro to Cyber Security

## Name: Josh Gray

### Task 1: Hashing

**Reminder Deliverable:** Is your `salted-data.csv` in this repository?

Answer the following in this file:

* How many unique users are in the data? - 49
* How many salts did you create? - 49
* How many possible combinations will I need to try to figure out the secret ID
  of all students (assume I know all potential secret IDs and have your 
  `salted-data.csv`) - 4.9 million 
* Instead of salts, if you were to use a nonce (unique number for each hashed
  field) how many possible combinations would I need to try? - 100,000 x M

 This is much harder than using a salt per user because:

Instead of 49 salts, there are as many unique nonces as there are secret identifiers.
The number of combinations scales with the dataset size instead of just the number of users.

* Given the above, if this quiz data were *actual* class data, say for example
  your final exam, how would you store this dataset?  Why? - Use HMAC-SHA256 with a secret key, Argon2, AES-256 encryption, and delete unnecessary data. - Can't brute force the hashes.

```bash
cut -d',' -f1 salted-data.csv | sort | uniq | wc -l

```

---

### Task 2: Crypto Mining

**Reminder Deliverable:** Is your "mining" code in this repository (`mining/`)?
**Reminder Deliverable:** Is your nonce + word combos in `coins.txt`?

Answer the following:

* Found: 22578wonderful - 0008b337ba22337f194c838895eafc8bde36fbc8c7b17259095e98cd13af2e8b
* 

```

```

* How many words were in your dictionary?
* How many nonces did your code iterate over?
* What was the maximum number of hashes your code *could* compute given the above?
* What did you think about Task 2?
* Is there a better way than brute force to attempt to get higher valued coins?
* Why or why not?


```bash
please put any cool bash one-liners or other piped commands you
learned/struggled with for task 2 here
```

