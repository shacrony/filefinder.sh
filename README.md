# filefinder.sh

lynx -dump "http://google.com/search?num=100&q=site:"$1"+ext:"$2""| grep ".$2" | cut -d "=" -f 2 | egrep -v "site|google" | sed s'/...$//'g

# usage:

sudo apt-get install lynx

git clone https://github.com/shacrony/filefinder.sh.git

chmod +x filefinder.sh

./filefinder.sh sitealvo.com.br pdf # pode ser qualquer extensão de arquivo

![filefinder](https://user-images.githubusercontent.com/61089592/173669678-987b6a0e-067f-4d43-b944-e62466813031.png)
