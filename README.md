# Emma
#Mini Games from python

@ramaalfiandi siapa tahu board-nya mau bisa diubah-ubah sesuai mode game-nya
def DisplayBoard(mod):
    #mode merupakan mode game, misal: 3 untuk 3x3, 10 untuk 10x10
    i = 0
    board =[x for x in range(1, (mod * mod)+1)]
        
    for y in range(1, (mod * 6) + 2):
        for x in range(1, (mod * 10) + 2):
            if y % 6 == 1:
                if x % 10 == 1:
                    print('+', end='')
                else:
                    print('-', end='')
            else:
                if x % 10 == 1:
                    print('|', end='')
                else:
                    if (x+4) % 10 == 0 and (y+2) % 6 == 0:
                        i += 1
                        if len(str(board[i-1])) >= 2:
                            print('', end='\x08' * (len(str(board[i-1])) - 1))
                            print(board[i-1], end='')
                        else:
                            print(board[i-1], end='')
                    else:
                        print(' ', end='')                
        print()
        
DisplayBoard(10)
 
