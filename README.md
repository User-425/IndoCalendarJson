
# Indonesian Calendar JSON Fetcher

This GitHub Action fetches JSON data from the kalenderindonesia.com API for the Gregorian calendar years from 1910 to 2100. It organizes the fetched data into a folder structure and commits it back to the repository.

### Workflow

The workflow is set to run every month and can also be manually triggered.

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

### How to use 
You can fetch the JSON by fetching the following url format
JSON per year:
```
https://raw.githubusercontent.com/User-425/IndoCalendarJson/main/json/[year]/data.json
```
Example usage (javascript):
```
fetch('https://raw.githubusercontent.com/User-425/IndoCalendarJson/main/json/2025/data.json')
    .then(res => res.json())
    .then((out) => {
        console.log('Output: ', out);
}).catch(err => console.error(err));
```

JSON per month:
```
https://raw.githubusercontent.com/User-425/IndoCalendarJson/main/json/[year]/[month]/data.json
```
Example usage (javascript):
```
fetch('https://raw.githubusercontent.com/User-425/IndoCalendarJson/main/json/2025/2/data.json')
    .then(res => res.json())
    .then((out) => {
        console.log('Output: ', out);
}).catch(err => console.error(err));
```
note: month index start from 0
