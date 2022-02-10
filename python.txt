# Python program to implement TPK algorithm
def f(x):
	return abs(x) ** 0.5 + 5 * x**3

def main():
	s = [7.9, 7.3, 20.9, 112.0, 5.0, 3.0, 2.9, 9.0, 21.7, 31.2, 4.1]
	s.reverse()
	i = 10
	for x in s:
		result = f(x)
		if result > 500:
			print('%d %s' % ("ans: " + i + " is greater than 500"))
			i = i-1
		else:
			print('%d %f' % (i, result))
			i = i-1
	print('')
	
if __name__ == '__main__':
	main()
