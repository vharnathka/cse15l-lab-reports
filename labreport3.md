# Lab Report 3

**Showing the different command-line options for the `grep` command**

When using `man grep`, the commands manual describes the `grep` command as a 'file pattern searcher'. It 'searches any given input files' and then selects 'lines that match one or more patterns'.

**Note: The command `grep -r` is often used alongside many of the command-line options below as it allows the user to search recursively through all subdirectories. This way the user does not have to search individually through each folder**

## -L
The `grep -L` command-line option is called 'files-without-matches'. Instead of printing the lines that match the specified pattern, it prints the names of the input files that didn't have any matches with the pattern.

This was taken from the [Linux manual page](https://man7.org/linux/man-pages/man1/grep.1.html).

Example 1:
```
$ cd non-fiction
$ cd OUP
$ cd Castro
$ grep -L "history" ./*
./chQ.txt
./chR.txt
./chV.txt
./chY.txt
./chZ.txt
```

Example 2:
```
$ cd non-fiction
$ cd OUP
$ grep -rL "history" ./*
./Abernathy/ch3.txt
./Abernathy/ch7.txt
./Abernathy/ch8.txt
./Abernathy/ch9.txt
./Abernathy/ch14.txt
./Berk/CH4.txt
./Berk/ch7.txt
./Castro/chR.txt
./Castro/chQ.txt
./Castro/chV.txt
./Castro/chZ.txt
./Castro/chY.txt
./Kauffman/ch3.txt
./Kauffman/ch1.txt
./Kauffman/ch4.txt
./Kauffman/ch5.txt
./Kauffman/ch8.txt
./Rybczynski/ch2.txt
./Rybczynski/ch1.txt
```

## -c

The `grep -c` command counts the number of matching lines in each file.

This was taken from the [Linux manual page](https://man7.org/linux/man-pages/man1/grep.1.html).

Example 1:
```
$ cd non-fiction
$ cd OUP
$ cd Berk
$ grep -c "intricate" ./CH4.txt
5
```

Example 2:
```
$ cd non-fiction
$ cd OUP
$ cd Fletcher
$ grep -c "reason" ./*
./ch1.txt:2
./ch10.txt:1
./ch2.txt:5
./ch5.txt:8
./ch6.txt:8
./ch9.txt:8
````

## "^ "
This command is executed by typing `grep "^x"` with x being any character. It returns the lines in that file that start with the specified character.

This command was found by typing 'tell me some interesting uses of the grep command' on ChatGPT.

Example 1:
```
$ cd non-fiction
$ cd OUP
$ cd Fletcher
$ grep "^b" ch2.txt
by the Bill of Rights 1791in 1865, 1868, and 1870
by History
```

Example 2:
```
$ cd non-fiction
$ cd OUP
$ cd Fletcher
$ grep "^[b-h]" ch2.txt
hundred and sixty three, and of the Independence of the
by the Bill of Rights 1791in 1865, 1868, and 1870
by History
divine mission
```

## -n

The `grep -n` command displays the line numbers along with the matching lines.

This was found by asking ChatGPT to show some interesting commands with grep.

Example 1:
```
$ cd travel_guides
$ cd berlitz2
$ grep -n "legislature" ./Nepal-History.txt
24:After King Birendra became sovereign in 1972 — tenth in the line of Shah rulers since King Prithvi the Great — a referendum in which all Nepalis over 21 were eligible to vote confirmed the popular preference for the panchayat system over a return to multi-party democracy. However, there was still some unrest regarding the issue. The king deferred to demands expressed in student demonstrations by making the majority of the legislature directly elected, with the council of ministers responsible to the parliament as well as to the king.
```

Example 2:
```
$ cd travel_guides
$ cd berlitz2
$ grep -rn "legislature" ./*
./California-History.txt:30:The Chinese arrived in the wake of the great Taiping Rebellion of 1851, seeking security and prosperity in what they were told were California’s “Golden Mountains.” They suffered both exploitation by Chinese entrepreneurs, who used them as indentured labor, and discriminatory taxation by the state legislature. The worst-treated, however, were the Native Americans, whose numbers dwindled rapidly not only as a result of disease and malnutrition but also because of systematic massacres in the 1850s by Californian militia.
./Canada-WhereToGo.txt:318:Starting in Confederation Plaza, visit Province House, the sober grey sandstone Georgian building in which the “Fathers of the Confederation” met in 1864. Originally a courthouse, it is now the seat of the provincial legislature. Confederation Chamber has been preserved with the names of the august delegates, a very dignified setting for an affair that was in fact characterized by somewhat extravagant wining and dining.
./Nepal-History.txt:24:After King Birendra became sovereign in 1972 — tenth in the line of Shah rulers since King Prithvi the Great — a referendum in which all Nepalis over 21 were eligible to vote confirmed the popular preference for the panchayat system over a return to multi-party democracy. However, there was still some unrest regarding the issue. The king deferred to demands expressed in student demonstrations by making the majority of the legislature directly elected, with the council of ministers responsible to the parliament as well as to the king.
./PuertoRico-History.txt:30:Politically, recent history is less conclusive. In 1951 the island’s voters approved a new constitution (still in effect) forming a commonwealth between the United States and the “free associated state” of Puerto Rico (though even the commencement ceremony was marred by violent demonstrations by radicals). As a result Puerto Ricans now elect their own governor, legislature, and local officials, and send a non-voting representative to the US Congress. In turn, Washington runs the postal, customs, and immigration services, handles defense and foreign relations, and sends dollars — particularly useful in times of crisis, such as after hurricanes.
```
