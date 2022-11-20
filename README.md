#lista de adyacencia

# A class to represent a graph object
class Graph:
	# Constructor
	def __init__(self, edges, n):
		# allocate memory for the adjacency list
		self.adjList = [[] for _ in range(n)]

		# add edges to the directed graph
		for (src, dest) in edges:
			# allocate node in adjacency list from src to dest
			self.adjList[src].append(dest)


# Function to print adjacency list representation of a graph
def printGraph(graph):
	for src in range(len(graph.adjList)):
		# print current vertex and all its neighboring vertices
		for dest in graph.adjList[src]:
			print(f'({src} —> {dest}) ', end='')
		print()


if __name__ == '__main__':

	
	edges = [(0, 1), (1, 2), (2, 0), (2, 1), (3, 2), (4,0),(4, 5), (4,9),(5,1),(5,3),(5, 4), (0,5),(3,5) , (6,0), (6,3) ,(1,6), (6,4), (8,1), (9,0),(7,0), (7,2),(7,5)]

	
	n = 12
	graph = Graph(edges, n)
	printGraph(graph)
