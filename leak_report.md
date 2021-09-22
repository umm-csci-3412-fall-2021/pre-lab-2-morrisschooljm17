# Leak report

_Use this document to describe whatever memory leaks
you find in `clean_whitespace.c` and how you might fix
them. You should also probably remove this explanatory
text._

**What caused the leak**: Memory being allocated to the result variable in line 41 within the strip function was never freed up.\
**How to solve the leak**: Free up the cleaned variable within the is_clean function before the return statement. This appeared to work until I recieved a error for an invalid free. To fix this, a conditional statement is created to check whether the cleaned variable is equal to an empty string.
