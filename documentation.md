# How to count the number of first names

## collect the data

Fetch the following data files:
```
curl https://www.nrscotland.gov.uk/files//statistics/babies-names/19/babies-first-names-top-100-boys.csv -o data/babies-first-names-top-100-boys.csv
curl https://www.nrscotland.gov.uk/files//statistics/babies-names/19/babies-first-names-top-100-girls.csv -o data/babies-first-names-top-100-girls.csv
```

## compute the number of firstnames

```
cp data/babies-first-names-top-100-girls.csv + data/babies-first-names-top-100-boys.csv data/all-names.txt
cat  data/babies-first-names-top-100-boys.csv >> data/all-names.txt 
cp data/all-names.txt input.txt
./data-pipeline.sh
cat output.txt
```

