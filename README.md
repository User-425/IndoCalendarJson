
# Indonesian Calendar JSON Fetcher

This GitHub Action fetches JSON data from the kalenderindonesia.com API for the Gregorian calendar years from 1910 to 2100. It organizes the fetched data into a folder structure and commits it back to the repository.

### Workflow

The workflow is set to run every 1st of December and can also be manually triggered.

### Folder Structure

The fetched JSON data is organized into the following folder structure:

```
json/
│
├── 1910/
│   ├── 0/             # January
│   ├── 1/             # February
│   ├── ...
│   └── 11/            # December
│
├── 1911/
│   ├── 0/             # January
│   ├── 1/             # February
│   ├── ...
│   └── 11/            # December
│
├── ...
│
└── 2100/
    ├── 0/             # January
    ├── 1/             # February
    ├── ...
    └── 11/            # December
```
