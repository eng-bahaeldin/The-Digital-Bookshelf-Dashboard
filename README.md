# The Digital Bookshelf Dashboard

A simple state-driven JavaScript application for managing and filtering a personal reading list. The dashboard displays books from a single source-of-truth array and updates the visible list when a filter is selected.

## Features

- Displays book titles, authors, and read status.
- Shows all books in their original order.
- Filters the collection by `All Books`, `Read`, or `Unread`.
- Highlights the currently selected filter.
- Re-renders the bookshelf from the current application state.
- Preserves the original `myBookshelfState` array when filters are used.
- Uses strict boolean checks for `isRead` values.

## How to Run

1. Open the project folder in VS Code.
2. Open `index.html` in a web browser.

No installation, build process, or external dependencies are required.

## How to Use

When the page loads, all books are displayed. Select one of the filter buttons to view only read books, only unread books, or the complete collection. Select `All Books` to restore the full bookshelf.

## Book Data Structure

Books are stored in the global `myBookshelfState` array. Each book follows this structure:

```javascript
{
	id: 1,
	title: "Book Title",
	author: "Book Author",
	isRead: true
}
```

Set `isRead` to `true` for a read book or `false` for an unread book.

## Main JavaScript Functions

### `filterBookshelf(booksArray, filterType)`

Returns the books that match the selected filter. The available filter values are:

- `"all"` - returns the complete array.
- `"read"` - returns books where `isRead` is exactly `true`.
- `"unread"` - returns books where `isRead` is exactly `false`.

### `renderBookshelf()`

Filters the current state, clears the display area, and creates the book cards shown on the page. The filter button event listeners call this function whenever the selected filter changes.

## Project Files

- `index.html` - Contains the page layout, styling, bookshelf state, filtering logic, rendering logic, and event listeners.
- `README.md` - Provides project documentation and usage instructions.
