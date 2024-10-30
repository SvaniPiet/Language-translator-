import tkinter as tk
from googletrans import Translator

class LanguageTranslator:
    def __init__(self, root):
        self.root = root
        self.root.title("Language Translator")
        self.root.geometry("500x400")

        # Create input fields
        self.src_language_label = tk.Label(root, text="Source Language:")
        self.src_language_label.pack()
        self.src_language_entry = tk.Entry(root, width=50)
        self.src_language_entry.pack()

        self.dest_language_label = tk.Label(root, text="Destination Language:")
        self.dest_language_label.pack()
        self.dest_language_entry = tk.Entry(root, width=50)
        self.dest_language_entry.pack()

        self.text_to_translate_label = tk.Label(root, text="Text to Translate:")
        self.text_to_translate_label.pack()
        self.text_to_translate_entry = tk.Text(root, width=50, height=7)
        self.text_to_translate_entry.pack()

        # Create translate button
        self.translate_button = tk.Button(root, text="Translate", command=self.translate_text)
        self.translate_button.pack()

        # Create output field
        self.translation_label = tk.Label(root, text="Translation:")
        self.translation_label.pack()
        self.translation_text = tk.Text(root, width=50, height=7)
        self.translation_text.pack()

    def translate_text(self):
        src_language = self.src_language_entry.get()
        dest_language = self.dest_language_entry.get()
        text_to_translate = self.text_to_translate_entry.get("1.0", "end-1c")

        translator = Translator()
        result = translator.translate(text_to_translate, src=src_language, dest=dest_language)
        translation = result.text

        self.translation_text.delete("1.0", "end")
        self.translation_text.insert("1.0", translation)

if __name__ == "__main__":
    root = tk.Tk()
    app = LanguageTranslator(root)
    root.mainloop()
