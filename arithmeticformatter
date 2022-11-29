def arithmetic_arranger(problems, result=False):

  firstl = ""
  secl = ""
  dashl = ""
  resl = ""
  final_string = ""

  if len(problems) > 5:
    return "Error: Too many problems."

  for op in problems:
    split = op.split()
    operator = split[1]
    if operator not in ['+', '-']:
      return "Error: Operator must be '+' or '-'."
    elif (len(split[0])>4) or (len(split[2])>4):
      return "Error: Numbers cannot be more than four digits."
    elif (split[0].isnumeric()==False) or (split[2].isnumeric()==False):
      return "Error: Numbers must only contain digits."

  for val in problems:
    split = val.split()
    operator = split[1]
    num1, num2 = int(split[0]), int(split[2])
    length = max(len(split[0]), len(split[2]))+2
    top = split[0].rjust(length)
    bottom = operator+split[2].rjust(length-1)
    dashlen = ""
    for s in range(length):
      dashlen += "-"

    if operator == "+":
      sol = num1 + num2
    else:
      sol = num1 - num2
      
    res = str(sol).rjust(length)

    if val != problems[-1]:
      firstl+= top + '    '
      secl+= bottom + '    '
      dashl+= dashlen + '    '
      resl+= str(sol) + '    '
    else:
      firstl+= top
      secl+= bottom
      dashl+= dashlen
      resl+= str(sol)
      
  if result == True:
    final_string += firstl + "\n" + secl + "\n" + dashl + "\n" + resl
  else:
    final_string += firstl + "\n" + secl + "\n" + dashl

  return final_string
