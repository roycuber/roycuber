from openpyxl.workbook import workbook
from openpyxl import load_workbook
import smtplib

#load existing spreadsheet

wb = load_workbook('test.xlsx')

#create an active worksheet
ws = wb.active

#grab a whole column
column_c = ws['C2':'C5'] #number of row(numbers, or column(letter+number, A2...))
#print(column_d)
#for loop
for cell in column_c: #cell is just a variable of our choice for the loop output
	for x in cell:
		if int(float(x.value)) < 30:
			print(f'{x.value}') #value gives the actual value from the cell rather then its position


