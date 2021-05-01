# Add default ssh key

## How to create ssh key

`1. ssh-keygen -C "mehedi609@gmail.com"`

press enter for all promt

it will create id_rsa and id_rsa.pub files in your .ssh dir in users dir

2. add the following code in your config file. If no config file is there than create a config file with no extension

```
#Account1
Host github.com
  HostName github.com
  IdentityFile ~/.ssh/id_rsa
```

4. in terminal write

`cat id_rsa.pub`

3. copy the content inside id_rsa.pub
    - open your github account.
    - go to settings and click SSH and GPG keys menu
    - click "New SSH key" button
    - give a title in input box
    - pass the key in the key box
    - press "Add SSH key" button
    
You are good to go.


# Add ssh key for another account (wok account)

## How to create ssh key

`1. ssh-keygen -f [any_name]_id_rsa -C "your_email@example.com"`

replace [any_name] with your desired name.

command may be like this

`ssh-keygen -f mehedibjit_id_rsa -C "hasan.mehedi@bjitgroup.com"`

press enter for all promt

it will create mehedibjit_id_rsa and mehedibjit_id_rsa.pub files in your .ssh dir in users dir

2. add the following code in your config file. If no config file is there than create a config file with no extension

```
#Account2
Host github.com-mehedibjit
  HostName github.com
  IdentityFile ~/.ssh/mehedibjit_id_rsa
```

4. your config file will be look like this

```
#Account1
Host github.com
  HostName github.com
  IdentityFile ~/.ssh/id_rsa
  
#Account2
Host github.com-mehedibjit
  HostName github.com
  IdentityFile ~/.ssh/mehedibjit_id_rsa
```

5. in terminal write

`cat mehedibjit_id_rsa.pub`

3. copy the content inside mehedibjit_id_rsa.pub
    - login in your another account
    - go to settings and click SSH and GPG keys menu
    - click "New SSH key" button
    - give a title in input box
    - pass the key in the key box
    - press "Add SSH key" button

You are good to go.
