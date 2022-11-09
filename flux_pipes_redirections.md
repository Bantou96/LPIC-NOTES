### Flux
- entrée standard (stdin)
- sortie standard (stdout)
- sortie d'erreur standard (stderr)

### Redirections
- > stdout vers un nouveau fichier 
- >> stdout à la suite d'un fichier 
- 2> stderr vers un nouveau fichier 
- 2>> stderr à la suite d'un fichier 
- &> stdout + stderr
- < stdin depuis un fichier 
- << stdin à partir d'une chaine de caractères
- <> stdin et stdout vers et depuis le même fichier 

### Pipe
- le caractère | : rediriger la sortie standard d'une commande vers l'entrée standard d'un autre 

### Utilisation et substition d'arguments
- xargs : permet de faire en sorte que la sortie de la première commande soit utiliser comme argument de la deuxième commande (ls | xargs rm)
- backquotes : remplacer de manière itérative la sortie d'une commande (rm `ls`) 
