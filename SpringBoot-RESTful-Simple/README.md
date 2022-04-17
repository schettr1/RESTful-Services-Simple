@RestController
public class BookController {

	Book book;
	
	@GetMapping(value="/books", produces="application/json")
	public List<Book> getBooks(){
		List<Book> books = new ArrayList<Book>();
		book = new Book(1, "English", "John");
		books.add(book);
		book = new Book(2, "Nepali", "Ruth");
		books.add(book);
		book = new Book(3, "Maths", "Monica");
		books.add(book);
		return books;
	}
}
