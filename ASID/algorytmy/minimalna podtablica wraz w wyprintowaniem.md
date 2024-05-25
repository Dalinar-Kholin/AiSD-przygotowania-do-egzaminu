poroblem znalezienia minimalnej podtablicy ma sens tylko gdy występują w niej liczby ujemne

idea algorytmu

idziemy liniowo po tablicy i zapamiętujemy największą sumę podtablicy oraz aktualną
oraz indexy zaczynjące
przechodząc do następnego elementu sprawdzamy czy opłaca nam się dodać ten element, jeżeli suma po jego dodaniu jest ujemna, to wiadomo że nie opłaca nam się go dodać co zarazem kończy naszą potencjalną najdłuższą podtablice i zaczyna nową

***właściwości***
 - liniowy - czasowo
 - stały pamięciowo - wykorzystujemy tylko 4 komórki pamięci



	def maxSubArraySum(a, size):

    max_so_far = -maxsize - 1
    max_ending_here = 0
    start = 0
    end = 0
    s = 0

    for i in range(0, size):

        max_ending_here += a[i]

        if max_so_far < max_ending_here:
            max_so_far = max_ending_here
            start = s
            end = i

        if max_ending_here < 0:
            max_ending_here = 0
            s = i+1

    print("Maximum contiguous sum is %d" % (max_so_far))
    print("Starting Index %d" % (start))
    print("Ending Index %d" % (end))