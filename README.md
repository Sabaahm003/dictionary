# dictionary

import tkinter as tk
def find_word_definition():
    word = entry.get()
    if word in english_dictionary:
        definition_text.set(english_dictionary[word])
    else:
        definition_text.set("Word not found in the dictionary")

english_dictionary ={

"hello": "used as a greeting",

"world": "the earth, together with all of its countries and peoples"

}
# ایجاد یک پنجره
window = tk.Tk()
window.title("English Dictionary")

# ایجاد ورودی برای وارد کردن واژه
entry = tk.Entry(window)
entry.pack()

# ایجاد دکمه برای جستجو
search_button = tk.Button(window, text="Search", command=find_word_definition)
search_button.pack()

# نمایش تعریف واژه
definition_text = tk.StringVar()
definition_label = tk.Label(window, textvariable=definition_text)
definition_label.pack()


window.mainloop()
exec(open('english_dictionary.py').read())
