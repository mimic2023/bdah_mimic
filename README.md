ReadMe file for the bdah_mimic repo.

- Environment Setup
1. Create the conda environment using the environment.yml file.
2. Install the PostgreSQL from the Postgresql website(https://www.postgresql.org/)
3. Go to PgAdmin and create a database called 'mimic' and create an user which will be used to execute the commands.


- Data Setup
1. Go to the folder code/sql/postgres_setup/buildmimic
2. Run the files: postgres_create_tables.sql, postgres_add_indexes.sql, postgres_add_constraints.sql, postgres_add_comments.sql, postgres_checks.sql
3. Download the mimic-iii data from the phsyionet website()
4. Load the data using the posgres_load_data_7zip.sql, modify the file as needed to ensure it is reading the files from the right folder.
5. Go to the folder code/sql/postgres_setup/concepts and run the files postgres_functions.sql, postgres-make-concepts.sql. Make-concepts file will take time to run.
6. Run the file niv-durations.sql in the code/sql/postgres_setup.

Sample command to run the sql files in windows - "psql -p 5433 -d mimic -f postgres-make-concepts.sql"

These steps complete the data loading into the postgresql.
