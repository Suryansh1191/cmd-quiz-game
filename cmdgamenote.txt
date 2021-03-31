@echo off
color 0A

:menu
cls
echo Hey! Welcome to the game!
echo 1) start
echo 2) Exit 
set /p number=
if %number% == 1 goto StartGame
if %number% == 2 goto exit

:startgame
cls
echo Type your name:
set /p name=
echo Hello %name%!
echo Do you want to start the quiz? (y/n)
set /p start=
if %start% == y goto level1
if %start% == n goto menu
goto startgame


:exit
echo Thanks for playing!
timeout 5
exit

:level1
cls 
echo Question 1: MLH Share is of how many weeks?
echo 1) 2 week
echo 2) 1 week
echo 3) 3 week
set /p answer1=
if %answer1% == 1 goto wrong1
if %answer1% == 2 goto correct1
if %answer1% == 3 goto wrong1

:correct1
cls
echo You are right! Next Level? (y/n)
set /p NL1=

if %NL1% == y goto level2
if %NL1% == n goto menu
goto correct1

:wrong1
cls
Echo Sadly, you were wrong Retry? (y/n)
set /p WA1=
if %WA1% == y goto level1
if %WA1% == n goto menu
goto wrong1

:level2
cls
echo question 2: how many steps does MLH share registration form have ?
echo 1) 5 steps
echo 2) 6 steps
echo 3) 1 steps
echo 4) 4 steps
set /p aa=
if %aa% == 1 goto correct2
if %aa% == 2 goto wrong2
if %aa% == 3 goto wrong2
if %aa% == 4 goto wrong2
goto correct2

:correct2
cls 
echo You are right! Next level? (y/n)
set /p ka=
if %ka% == y goto level3
if %ka% == n goto menu

:wrong2
cls
echo Sadly, you were wrong Retry? (y/n)
set/p retry=
if %retry% == y goto level3
if %retry% == n goto menu

:level3
cls
echo question 3: which is the best guild in MLH share?
echo 1) 🦈 BLAHAJGang 🦈	
echo 2) Developer Student Community	
echo 3) Technocrats
set /p ka=
if %ka% == 1) goto wrong3
if %ka% == 2) goto correct3
if %ka% == 3) goto wrong3
goto correct3

:correct3
cls
echo You are correct XD ! You won the game!
goto exit

:wrong3
cls
echo sadly, you were wrong Retry? (y/n)
set/p retry=
if %retry% == y goto level3
if %retry% == n goto exit            