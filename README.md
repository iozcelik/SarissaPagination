# @sarissa/pagination

<a href="https://stackblitz.com/github/iozcelik/SarissaPagination" rel="nofollow"><img src="https://user-images.githubusercontent.com/10682780/163113951-9e30911b-bc57-4cbe-a837-f59053cf0355.svg" alt="Open in StackBlitz" data-canonical-src="https://developer.stackblitz.com/img/open_in_stackblitz.svg" style="max-width: 100%;"></a>

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
outerDiv | Outer div style of pagination buttons (default: flex items-center justify-center)
buttonGroup | Style of button group (no default)
button | Style of all page number buttons (default: relative flex-nowrap inline-flex items-center px-4 py-2 border text-sm font-medium)
activeButton | Style of active page button (default: bg-sky-500 text-white)
disabledButton | Style of disabled buttons (default: disabled:opacity-75)
currentPage | Current page number (required)
totalPage | Total page numbers (required)
url | Url of slug (required. ex: 'post','categories')
