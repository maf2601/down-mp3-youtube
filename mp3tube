# Este código tem como objetivo realizar o download do vídeo -> mp4, converter para áudio -> mp3, depois exclui o mp4 baixado #
# Para rodar este código e necessário instalar: #
# Pytube -> pip install pytube #
# Moviepy -> pip install moviepy #

from pytube import Youtube
import moviepy.editor as mp
import re
import os

# Digite o link do vídeo e o local que deseja salvar o mp3 #
link = input("Digite o link do vídeo que deseja baixar: ")
path = input("Digite a pasta que deseja salvar o vídeo: ")
yt = YouTube(link)

print("Iniciando o download...")
print("Download Completo!")

# Começa o download mp4 para mp3 #
print('Convertendo aquivo...")
for file in os.listdir(path):
    if re.search('mp4', file):
        mp4_path = os.path.join(path, file)
        mp3_path = os.path.join(path, os.path.splitext(file)[0]+'.mp3')
        new_file = mp.AudioFileClip(mp3_path)
        os.remove(mp4_path)
print('Concluído com Sucesso!')
