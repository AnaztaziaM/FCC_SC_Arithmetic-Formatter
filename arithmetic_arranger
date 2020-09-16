def arithmetic_arranger(problems, ft=False):
    count = len(problems)
    # Searching for errors.
    if count > 5:
        return "Error: Too many problems."
    for items in problems:
        i = items.split()
        if i[1] != "+" and i[1] != "-":
            return "Error: Operator must be '+' or '-'."
        elif len(i[0]) > 4:
            return "Error: Numbers cannot be more than four digits."
        elif len(i[2]) > 4:
            return "Error: Numbers cannot be more than four digits."
        if i[0].isnumeric() and i[2].isnumeric():
            continue
        else:
            return "Error: Numbers must only contain digits."

    # Display the numbers.

    # Display the firs line.
    first_line = []
    for x in problems:
        a = x.split()
        w_first = max(len(a[0]), len(a[2])) + 2
        aa=str(a[0].rjust(w_first)+"   ")
        first_line.append(aa)
    firs_line_printable = ' '.join([str(elem) for elem in first_line])

    # Display the second line.
    second_line = []
    for y in problems:
        b = y.split()
        t = len(b[0])
        tt = len(b[2])
        w_second = max(len(b[0]), len(b[2])) + 2
        if tt >= t:
            aaa=str((b[1]+(' ')+ b[2]).rjust(w_second)+"   ")
            second_line.append(aaa)
        elif t >= tt:
            aaaa=str((b[1]+(w_second-(len(b[2])+1))*(' ')+ b[2]).rjust(w_second)+"   ")
            second_line.append(aaaa)
    second_line_printable = ' '.join([str(elem) for elem in second_line])


    #Display the dash line.
    dash_line = []
    for z in problems:
        c = z.split()
        w_third = max(len(c[0]), len(c[2])) + 2
        dash = w_third*"-"
        dd=str(dash.rjust(w_third) + "   ")
        dash_line.append(dd)
    dash_line_printable = ' '.join([str(elem) for elem in dash_line])


    # Display the result.

    if ft:
        final_result = []
        for r in problems:
            d = r.split()
            w_forth = max(len(d[0]), len(d[2])) + 2
            if d[1] == "+" or "-":
                if d[1] == "+":
                    e = int(d[0]) + int(d[2])
                if d[1] == "-":
                    e = int(d[0]) - int(d[2])
                result = str(e)
                ff=str(result.rjust(w_forth) + "   ")
                final_result.append(ff)
        final_result_printable = ' '.join([str(elem) for elem in final_result])
        with_result=str(firs_line_printable.rstrip()+"\n"+second_line_printable.rstrip()+"\n"+dash_line_printable.rstrip()+"\n"+final_result_printable.rstrip())
        return with_result
    else:
        without_result=str(firs_line_printable.rstrip() + "\n" + second_line_printable.rstrip() + "\n" + dash_line_printable.rstrip())
        return without_result
