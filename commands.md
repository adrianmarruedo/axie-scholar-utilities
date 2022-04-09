
###  Generate Payments
Watchout, it adds a weird character at the beggining of Name field

    docker-compose run scholar-utilities generate_payments files/csv_payments_file.csv files/payments.json

###  Generate Secrets
Not very useful

    docker-compose run scholar-utilities generate_secrets files/payments.json files/secrets.json 

### Mass Update
Watch out, it adds the first pair with a weird character at the beggining of the key.

    docker-compose run scholar-utilities mass_update_secrets files/mass_update.csv files/secrets.json

### Claim SLP

    docker-compose run scholar-utilities claim files/payments.json files/secrets.json

### Payout

    docker-compose run scholar-utilities payout files/payments.json files/secrets.json -y