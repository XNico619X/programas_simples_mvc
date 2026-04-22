from vista import BibliotecaVista

class BibliotecaControlador:
    def __init__(self, libros):
        self.libros = libros
        self.vista = BibliotecaVista()

    def prestar(self, indice):
        if 0 <= indice < len(self.libros):
            libro = self.libros[indice]
            if libro.disponible:
                libro.disponible = False
                self.vista.mostrar_mensaje(f"Prestado: {libro.titulo}")
            else:
                self.vista.mostrar_mensaje("Ya está prestado.")
        else:
            self.vista.mostrar_mensaje("Índice no válido.")

    def devolver(self, indice):
        if 0 <= indice < len(self.libros):
            self.libros[indice].disponible = True
            self.vista.mostrar_mensaje(f"Devuelto: {self.libros[indice].titulo}")
