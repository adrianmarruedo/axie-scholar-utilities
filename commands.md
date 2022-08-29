
###  Generate Payments
Watchout, it adds a weird character at the beggining of Name field

    docker-compose run scholar-utilities generate_payments files/csv_payments_file.csv files/payments.json

###  Generate Secrets
Not very useful

    docker-compose run scholar-utilities generate_secrets files/payments.json files/secrets.json 

### Mass Update
Watch out, it adds the first pair with a weird character at the beggining of the key.

    docker-compose run scholar-utilities mass_update_secrets files/mass_update.csv files/secrets.json

### Scatter
In order to have RON enough for the gas fees.

    docker-compose run scholar-utilities scatter_ron files/payments.json files/secrets.json MIN_RON

### Claim SLP

    docker-compose run scholar-utilities claim files/payments.json files/secrets.json
In case of error

    docker-compose run scholar-utilities claim files/payments.json files/secrets.json --force

### Payout SLP

    docker-compose run scholar-utilities payout files/payments.json files/secrets.json -y

### Payout AXS

    docker-compose run scholar-utilities payout_axs files/payments.json files/secrets.json -y