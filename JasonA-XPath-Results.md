## XPath
# Employee Overview:
•	Select all tds that have money sign in them
-	hint Use contains()

``
		//td[contains(text(), '$')]
``

	$72,000
	$95,000
	$51,000
	$72,000

•	Get the first tr in the tbody
-	hint Use position

``
//tbody/tr[position()=1]
``

	101, Billy, Bobson, Sales, $72,000

•	Get the last tr in the tbody
-	hint use last()

``
//tbody/tr[last()]
``

	404, Bobby, Billson, Sales, $72,000

•	Get All tds where the id is between 200 and 300
-	hint use logical operators and [@id]

``
//td[@id > 200 and @id < 300]
``

	202, Alucard, Schmacula, Employee Engagement, $95,000
	203, Tim, Smith, IT $51,000

 
# Hi Score:
•	Get the li that conatins TIM's Dig Dug score
-	hint use 'and'

``
//li[contains(text(), "TIM") and contains(text(), "Dig")]
``

	TIM, 875, Dig Dug

•	Get the list items that belong to YVN or GAR

``
//li[contains(text(), "YVN") or contains(text(), "GAR")]
``

	GAR, 99999, Dig Dug
	YVN, 7000, Pac-man
	YVN, 5000, Pac-man

•	Get the total amount of li in the document
-	hint use count

``
console: $x("count(//li)") 
``

	There are 8 li
 
# Sales Report:
•	Select only the second table

``
(//table)[2]
``

		Selects only the second table.

•	Select all trs where the attribute data-leader="Margaret"

``
//tr[@data-leader = "Margaret"]
``

	Table 1:
	Thin Mints, 134, Westview Middle
	Table 2:
	Thin Mints, 61, Westview Middle
	Lemon Ups, 163, Springvale Prep

•	Select all the tds containing the sales where Westview Middle was the troop
-	hint use parent

``
//td[../td[contains(text(), 'Westview Middle')]][2]
``

	Table 1:
	Thin Mints, 134, Westview Middle
	Tagalongs, 98, Westview Middle
	Lemon, 67, Westview Middle
	Table 2:
	Thin Mints, 61, Westview Middle
	Tagalongs, 41, Westview Middle
	Lemon, 19, Westview Middle

•	Select the last tr of Thin Mints in the first half

``
(//table)[1]//tr[./td[contains(text(), 'Thin Mints')]][last()]
``

	Thin Mints, 22, Fulton Elementary

