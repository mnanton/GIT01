># PRACTICA DEL CURSO DE GIT
>>##  Preguntas Ejercicio 1
## **¿Qué comando utilizaste en el paso 11? ¿Por qué?**
*git reset --hard HEAD~1*   
// Se ha utilizado el parámetro --hard, ya que se solicitó también eliminar el working copy.

## **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
*git reflog*  
// Se busca el identificador del Commit (45485d5)
*git reset --hard 45485d5*

## **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
*git merge main*  
// Devuelve "Already up to Date".La rama que intentamos fusionar es **padre** de la rama actual.

## **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
*CONFLICT (content): Merge conflict in git-nuestro.md*   
// Las ramas a fusionar contienen el mismo archivo, pero con diferente contenido.

## **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
*No, La rama es **padre** de la rama actual.*

## **¿Qué comando o comandos utilizaste en el paso 25?**
*git log --graph --oneline*

## **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
*Si, la rama que intentamos fusionar es **padre** de la rama actual. *

## **¿Qué comando o comandos utilizaste en el paso 27?**
*git reset HEAD~1*

## **¿Qué comando o comandos utilizaste en el paso 28?**
*git add git-nuestro.md*, pàra sobreescribir el archivo

## **¿Qué comando o comandos utilizaste en el paso 29?**
*git branch -D title*

## **¿Qué comando o comandos utilizaste en el paso 30?**
*git branch title*  
*git switch title*  
*git reflog*   
// Obtenemos el Hash (e8f8191)  
*git checkout e8f8191*  
*git reset e8f8191*  
*git restore git-nuestro.md*  
*git switch main*  
*git merge title --no-ff*  

## **¿Qué comando o comandos usaste en el paso 32?**
*git checkout b2e667b*  

## **¿Qué comando o comandos usaste en el punto 33?**
*git checkout 36acdc*  


># PRACTICA DEL CURSO DE GIT
>>##  Secuencia Ejercicio 1

01.- git init --initial-branch=main  

02.- nano git-nuestro.md  

03.- git add git-nuestro.md  

04.- git commit -m "main - First Commit"  

05.- git branch styled  

06.- git branch  

07.- git switch styled  

08.- git status // git branch  

09.- nano git-nuestro.md  

10.- git add git-nuestro.md  
     git commit -m "styled - First Commit"  

11.- git reset --hard HEAD~1  

12.- git reflog // Obtenemos el Hash (45485d5)  
     git reset --hard 45485d5  

13.- git merge main  

14.- git switch main  

15.- git branch htmlify  

16.- git switch htmlify  

17.- nano git-nuestro.md  

18.- git add git-nuestro.md  
     git commit -m "htmlify - First Commit"  

19.- git switch styled  
     git merge htmlify  

20.- nano git-nuestro.md  
     // Resolver conflictos  
     git add git-nuestro.md  
     git commit  

21.- git switch main  
     git merge styled  

22.- git branch title  
     git switch title  

23.- nano git-nuestro.md  
     // Se añade Modificación Rama title  
     git add git-nuestro.md  
     git commit -m "title - First Commit"  

24.- git switch main  

25.- git log --graph --oneline  
[Diagrama Git](./assets/Diagram1.PNG)  
[Diagrama Visual Studio Code](./assets/Diagram1.PNG)  

26.- git merge title --no-ff  
[Diagrama Paso 26](./assets/Diagram3.PNG)  

27.- git reset HEAD~1  

28.- git add git-nuestro.md  

29.- git branch -D title  

30.- git branch title  
     git switch title  
     git reflog  
     // Obtenemos el Hash (e8f8191)  
     git checkout e8f8191  
     git reset e8f8191  
     git restore git-nuestro.md  
     git switch main  
     git merge title --no-ff  

31.- git branch main  
     // Aunque ya estabamos en la misma rama  
     git branch -d title  
     git branch -d styled  
     git branch -d htmlify  

32.- git checkout b2e667b  

33.- git checkout 36acdc  

34.- git reflog  
     // Obtenemos los Hash  
     git tag inicial b2e667b  
     git tag styled 45485d5  
     git tag htmlify b2e667b  
     git tag title 5e07414  

35.- git checkout htmlify  