# MAGAMZINE
def calculate_averages(matrix, R, C):
    max_in_rows = [max(row) for row in matrix]
    average_max_in_rows = sum(max_in_rows) / R
    max_in_columns = [max(matrix[i][j] for i in range(R)) for j in range(C)]
    average_max_in_columns = sum(max_in_columns) / C
    return average_max_in_rows, average_max_in_columns
R, C = map(int, input().split())
matrix = [list(map(int, input().split())) for _ in range(R)]
average_max_in_rows, average_max_in_columns = calculate_averages(matrix, R, C)
print(f"{average_max_in_rows:.2f}")
print(f"{average_max_in_columns:.2f}")
