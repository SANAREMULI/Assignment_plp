
school_name = "Aitong Primary School"      # str      -> text
student_name = "Naserian Sankale"          # str
age = 14                                   # int      -> whole number
admission_number = 1042                    # int
term_fee = 8500.50                         # float    -> decimal number
fees_paid = False                          # bool     -> True / False
guardian_phone = None                      # NoneType -> "no value yet"

print("--- 1. Variables and data types ---")
print(student_name, "->", type(student_name))
print(age, "->", type(age))
print(term_fee, "->", type(term_fee))
print(fees_paid, "->", type(fees_paid))
print(guardian_phone, "->", type(guardian_phone))

amount_paid = 5000.00
balance = term_fee - amount_paid        # subtraction
annual_fee = term_fee * 3               # multiplication (3 terms a year)
monthly_average = annual_fee / 12       # division -> result is always float

total_students = 47
desks_per_row = 4
full_rows = total_students // desks_per_row        # floor division -> 11
students_left_over = total_students % desks_per_row  # modulus (remainder) -> 3
power_example = 2 ** 3                  # exponent: 2 to the power 3 -> 8

print("\n--- 2. Arithmetic operators ---")
print("Balance owed: ", term_fee, "-", amount_paid, "=", balance)
print("Annual fee (x3 terms):", annual_fee)
print("Monthly average:", round(monthly_average, 2))
print("Full desk rows:", full_rows, "| students left over:", students_left_over)
print("2 ** 3 =", power_example)


enrolled_count = 0                     # plain assignment
enrolled_count = enrolled_count + 1    # the long way to add 1
enrolled_count += 1                    # shorthand for the line above (now 2)

ict_lab_slots = 20
ict_lab_slots -= 1                     # Naserian takes one slot -> 19

print("\n--- 3. Assignment operators ---")
print("Students enrolled today:", enrolled_count)
print("ICT lab slots remaining:", ict_lab_slots)

class_capacity = 50
has_space = enrolled_count < class_capacity   # True
meets_min_age = age >= 6                      # True
below_max_age = age <= 17                     # True
still_owes = balance > 0                      # True

print("\n--- 4. Comparison operators ---")
print("age == 14:", age == 14)
print("age != 18:", age != 18)
print("Space in class:", has_space)
print("Still owes fees:", still_owes)


can_enrol = has_space and meets_min_age and below_max_age
needs_finance_followup = still_owes or (not fees_paid)

print("\n--- 5. Logical operators ---")
print("Can enrol:", can_enrol)
print("Finance follow-up needed:", needs_finance_followup)


subjects = ["Mathematics", "English", "Kiswahili", "Science"]  # list: ordered, editable
subjects.append("ICT")

term_dates = ("2026-01-05", "2026-04-04")  # tuple: ordered, cannot be changed

student_record = {                         # dict: key -> value pairs
    "name": student_name,
    "adm_no": admission_number,
    "age": age,
    "balance": balance,
}

streams = {"East", "West", "East"}         # set: duplicates removed -> 2 items

print("\n--- 6. Collections ---")
print("Subjects:", subjects)
print("Term runs:", term_dates[0], "to", term_dates[1])
print("Record:", student_record)
print("Streams:", streams)


offers_ict = "ICT" in subjects        # True
no_music = "Music" not in subjects    # True

print("\n--- 7. Membership operators ---")
print("School offers ICT:", offers_ict)
print("Music not offered:", no_music)

age_from_form = "15"                       # str, e.g. typed into a form
age_next_year = int(age_from_form) + 1     # str -> int, then add
fee_as_text = str(term_fee)                # float -> str, for messages
shillings_only = int(balance)              # float -> int drops decimals (no rounding)

print("\n--- 8. Type conversion ---")
print("'15' + 1 after casting:", age_next_year)
print("Fee as text:", fee_as_text, "->", type(fee_as_text))
print("Balance in whole shillings:", shillings_only)

print(f"\n=== {school_name}: Enrolment Summary ===")
print(f"Student: {student_name} (Adm {admission_number}), age {age}")
print(f"Fee balance: KES {balance:,.2f} | Fees cleared: {fees_paid}")
print(f"Eligible to enrol: {can_enrol}")
print(f"Finance follow-up needed: {needs_finance_followup}")
