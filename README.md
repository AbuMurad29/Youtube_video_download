from pytube import YouTube
from tkinter import filedialog
url_input = input("Pleas Enter Your URL :")
all_streams = YouTube(url_input).streams.all()
v = -1
for i in all_streams:
    v=v+1
    print(str(v)+" : "+str(i))
stn_input = int(input("Pleas Choose The Suitable Stream : "))
print("Pleas Choose Directory To Save :)")
folder_name = filedialog.askdirectory()
choice = all_streams[stn_input].download(folder_name)
print("Download Complete..............")
