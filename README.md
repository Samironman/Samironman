import tkinter as tk
from PIL import Image, ImageTk
import time

class AvengersClock:
    def __init__(self, root):
        self.root = root
        self.root.title("Avengers Clock")
        self.root.geometry("400x400")

        self.label = tk.Label(self.root, font=("Helvetica", 48), bg="black", fg="white")
        self.label.pack(fill=tk.BOTH, expand=True)

        self.update_time()

    def update_time(self):
        current_time = time.strftime("%H:%M:%S")
        self.label.config(text=current_time)
        self.label.after(1000, self.update_time)

def main():
    root = tk.Tk()
    clock = AvengersClock(root)
    root.mainloop()

if __name__ == "__main__":
    main()
!---
Samironman/Samironman is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
