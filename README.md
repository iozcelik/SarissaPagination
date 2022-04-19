# @sarissa/pagination

Add page number buttons for pagination. Automaticly add and disable numbers as current page number.

<img width="505" alt="image" src="https://user-images.githubusercontent.com/10682780/162905825-223f3257-c2a9-494d-bc56-ddcb075ec2f4.png">

## Installation
```js
npm install @sarissa/pagination
```

## Usage
```js
import { Pagination } from "@sarissa/pagination";

//Must set your total page count
const totalPage = 10;
---
<style is:global>
      .activeButton {
        --tw-bg-opacity: 1;
        background-color: rgb(239 68 68 / var(--tw-bg-opacity));
        color: wheat;
      }
</style>

<Pagination currentPage="1" {totalPage} url="posts" />

<Pagination currentPage="3" {totalPage} url="posts" activeButton="activeButton"
    />
```

### Component Props

Name | Description
--- | --- 
outerDiv | Outer div classes of pagination buttons (default: flex items-center justify-center)
buttonGroup | Classes of button group (no default)
button | Classes of all page number buttons (default: relative flex-nowrap inline-flex items-center px-4 py-2 border text-sm font-medium)
activeButton | Classes of active page button (default: bg-sky-500 text-white)
disabledButton | Classes of disabled buttons (default: disabled:opacity-75)
currentPage | Current page number (required)
totalPage | Total page numbers (required)
url | Url of slug (required. ex: 'post','categories')
