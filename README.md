luga37.github.io
a=int(input("Количество сдаваемых книг"))
b=int(input("Количество взятых книг"))
class Librarian:
    def __init__(self, name="Ivan", last_name="Ivanov", class_number="10B"):
        self.name = name
        self.last_name = last_name
        self.class_number = class_number
        self.library_books = 0
    
    def drop_off_books(self, books):
        self.library_books += books
    
    def collect_books(self, books):
        self.library_books -= books

    def check_books(self):
        if self.library_books < 0:
            print(f'{self.name} {self.last_name} {self.class_number} имеет недостаток в {abs(self.library_books)} книги!')
        else:
            print(f'{self.name} {self.last_name} {self.class_number} Недостатка нет!')
ivan = Librarian()
ivan.drop_off_books(a)
ivan.collect_books(b)
ivan.check_books()

