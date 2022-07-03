## Python-mini-project
##Chess Board

board = chess.Board("5r2/8/Kpk5/P5R1/8/8/8/8")
print(board)

a=input("Enter the move:")
if a=='rA8':
    print("Correct")
    board = chess.Board("r7/8/Kpk5/P5R1/8/8/8/8")
    print(board)
else:
    print("incorrect")
