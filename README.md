# THANOS

A Linux command line to kill half processes running on your computer with the snap of your fingers.

Simply place this line in your ~/.bashrc or ~/.zshrc etc... :

```bash
alias thanos="ps -eo pid | xargs -I{} bash -c 'if [ \$((RANDOM%2)) -eq 0 ]; then echo \"{} dies\" && kill -9 {}"; else echo \"{} lives\";fi'"
```

then call the **thanos** command and hit enter. All your running processes will be candidate for immolation with a 50% probability regardless of their CPU usage, wealth, skin color etc... freeing your CPU for the others to prosper.

You may optionnally call it with *sudo* to purify root or other people's processes too.

# Note

Use it when your CPU is overwhelmed and you don't have any data to lose or a robot running in real life depending on your PC's state and if the idea of blasting your OS it makes you feel good.

Other than that, don't use it. It's **stupid**.
