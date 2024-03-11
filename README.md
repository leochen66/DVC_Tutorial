# DVC_Tutorial

### Install DVC on mac
```
brew install dvc
```

### Init DVC in Repo
```
dvc init
```
This will create dvc files.

### Init File Access to Google Drive
```
dvc remote add -d myremote dgrive://<FOLDER_TOKEN>
```

```
git add .
git commit 
git push
```

### Generate Dataset
```
python get_data.py
```

### Update the Dataset
```
// This create data.csv.dvc file which tracks the status of your data file.
dvc add data.csv

git add .gitignore data.csv.dvc
git commit
git push

dvc push
```

### Pull Data from Remote Storage
```
dvc pull data.csv
```

### Reverse Dataset
```
git checkout HEAD^1 data.csv.dvc
dvc checkout

git commit 
git push
```