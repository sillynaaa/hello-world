# hello-world
set {year:y, month:m, day:d} to (current date)
display dialog "Enter day of birth." default answer ""
set BirthdayDay to text returned of (display dialog "Enter Day of Birth" default answer "")
set BirthMonth to (choose from list {"January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"} with prompt "Please Choose Birthday Month")
set BirthYear to text returned of (display dialog "Enter four digit birth year" default answer "")
set UserBirthDay to BirthMonth & " " & BirthdayDay & "," & BirthYear as string
set Birthdate to date UserBirthDay
set theMonthNumber to ((month of Birthdate as integer) as string)
set UserAge to y - (year of Birthdate)
set daysleft to (day of Birthdate) - d
set monthleft to (theMonthNumber) - m
if daysleft < 0 then
set daysleft to daysleft / -1 as integer
end if
if monthleft < 0 then
set monthleft to monthleft + 12

else
set UserAge to UserAge - 1
end if
set BirtdayInfo to "You are currently...

" & UserAge & " years old

" & "There are...

" & monthleft & " months and

" & daysleft & " days " & "left until your birthday"
