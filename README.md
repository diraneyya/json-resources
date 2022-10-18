# JSON resources
A collection of JSON data files that can be fetched using the Fetch API, available as ES6 and CommonJS modules for experimentation both from the Browser Console or the Node REPL.

## Books database

> _Source:_ https://github.com/benoitvallon/100-best-books/blob/master/books.json

_TypeScript Schema:_
```typescript
interface BookDatabaseEntry {
    author: 'Unknown' | string,
    country: string,
    // The image link is relative to this URL:
    // https://raw.githubusercontent.com/benoitvallon/100-best-books/master/static
    imageLink: string,
    // This is an absolute URL (i.e. Wikipedia)
    link: string,
    pages: number,
    title: string,
    year: number,
}

type BookDatabase = BookDatabaseEntry[];
```

### Browser DevTools (Console)

Navigate to [this page](https://diraneyya.github.io/json-resources/) first _before launching the DevTools' Console_:

```
books_resource = await fetch('https://diraneyya.github.io/json-resources/books.json');
books_database = await books_resource.json();       /* this is of type BookDatabase */
```