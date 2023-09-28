# Git Tips

```
 ssh-keygen -t rsa -b 4096 -C "sivan.moodley02@gmail.com" -f id_Teamfu
   62  eval "$(ssh-agent -s)"
   63  ssh-add id_Teamfu
   64  ssh-add -l
   65  git config --global user.name "Noisyninja703"
   66  git config --global user.email "sivan.moodley02@gmail.com"
   67  git config --global color.ui auto
   68  ssh -T git@github.com
   69  cat id_Teamfu.pub 
   70  ssh -T git@github.com
   71  cd -
   72  cd ~
   73  mkdir dev && cd dev
   74  git clone git@github.com:Noisyninja703/ever-wiki.git
   75  sudo snap install code --classic
   76  sudo snap list
   77  cd ever-wiki/
   78  code .
   79  history

```