# Jawaban Algoritma Test
1. Terdapat string "NEGIE1", silahkan reverse alphabet nya dengan angka tetap diakhir kata Hasil = "EIGEN1"

Code With Python :
```
# Definisikan string asli
original_string = "NEGIE1"

# Pisahkan bagian yang akan dibalik dan bagian yang tetap
part_to_reverse = original_string[:5]
part_to_keep = original_string[5:]

# Balikkan bagian yang perlu dibalik
reversed_part = part_to_reverse[::-1]

# Gabungkan kembali kedua bagian
result_string = reversed_part + part_to_keep

# Tampilkan hasil
print(result_string)
```
2. Diberikan contoh sebuah kalimat, silahkan cari kata terpanjang dari kalimat tersebut, jika ada kata dengan panjang yang sama silahkan ambil salah satu

Code With Python :
```
# Definisikan kalimat asli
sentence = "Saya sangat senang mengerjakan soal algoritma"

# Pisahkan kalimat menjadi daftar kata-kata
words = sentence.split()

# Inisialisasi variabel untuk kata terpanjang dan panjang maksimal
longest_word = ""
max_length = 0

# Iterasi melalui daftar kata-kata untuk menemukan kata terpanjang
for word in words:
    if len(word) > max_length:
        longest_word = word
        max_length = len(word)

# Tampilkan hasil
print(longest_word,":", max_length, "karakter")
```
3. Terdapat dua buah array yaitu array INPUT dan array QUERY, silahkan tentukan berapa kali kata dalam QUERY terdapat pada array INPUT

Code With Python :
```
# Definisikan array INPUT dan QUERY
INPUT = ['xc', 'dz', 'bbb', 'dz']
QUERY = ['bbb', 'ac', 'dz']

# Inisialisasi array OUTPUT
OUTPUT = []

# Iterasi melalui setiap kata dalam QUERY
for query_word in QUERY:
    # Hitung berapa kali query_word muncul dalam INPUT
    count = INPUT.count(query_word)
    # Tambahkan hasil hitungan ke OUTPUT
    OUTPUT.append(count)

# Tampilkan hasil
print("OUTPUT=", OUTPUT, "karena kata 'bbb' terdapat 1 pada INPUT, kata 'ac' tidak ada pada INPUT, dan kata 'dz' terdapat 2 pada INPUT")
```
4. Silahkan cari hasil dari pengurangan dari jumlah diagonal sebuah matrik NxN

Code With Python :
```
def diagonal_difference(matrix):
    n = len(matrix)
    primary_diagonal_sum = 0
    secondary_diagonal_sum = 0
    
    for i in range(n):
        primary_diagonal_sum += matrix[i][i]
        secondary_diagonal_sum += matrix[i][n - 1 - i]
    
    return abs(primary_diagonal_sum - secondary_diagonal_sum)

# Contoh matriks
matrix = [[1, 2, 0], [4, 5, 6], [7, 8, 9]]

# Hitung hasil pengurangan dari jumlah diagonal
result = diagonal_difference(matrix)

# Tampilkan hasil
print("hasilnya adalah 15 - 12 =", result)
