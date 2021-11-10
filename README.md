# Tugas-Praktikum-2-C-Function-Project-based-
Sep 20, 2021

1. Deklarasi, definisi, dan pemanggilan fungsi buatan sendiri (minimal terdapat 1 fungsi buatan sendiri, fungsi main() tidak terhitung)
2. Menggunakan salah satu dari fungsi standard C berikut: sprintf, sscanf, rand, strcmp, strstr, strcat
3. Hindari warning "implicit declaration" dengan cara: pastikan sudah menambahkan #include yang sesuai dengan fungsi yang dipanggil (untuk fungsi-fungsi pada C standard library) atau deklarasikan/definisikan fungsi terlebih dahulu sebelum dilakukan pemanggilan fungsi yang bersangkutan (*)


          #include <stdio.h>
          #include <stdlib.h>
          #include <time.h>


          int gacha_eq (int level, int jawaban, int ulang)
          {
              int x;{
                  x = rand() %10 + 1;
                  printf("%d ", x);
              }
          }



          int main() {
              char jawaban;
              int level, ulang;

              printf("~~~~~~~Gacha Equipment~~~~~~~\n\n");
              printf("\nGunakan 1 Soul Pearl untuk 1x Gacha?\n");
              printf ("Jawab(y/t) : ");
              scanf (" %c", &jawaban);

              if (jawaban == 'y'){
                  while (jawaban=='y'){
                     srand (time(NULL));
                      printf ("\n\n==========Selamat anda mendapatkan Equipment level "); gacha_eq(level, jawaban, ulang); printf("Dari Gacha Equipment==========\n\n");
                      printf ("\n\nApakah Ingin Menggunakan 1 Soul Pearl Untuk Gacha lagi?\n");
                      printf ("Jawab(y/t) : ");
                      scanf (" %c", &jawaban);

              while (jawaban=='t'){
                printf ("\n\nGacha Selesai Terimakasih!\n\n");
                break;
                }
              while ((jawaban != 't') && (jawaban != 'y')){
                  printf("\n\nMaaf Format Salah");
                  break;
              }
            }
          }



              else if (jawaban=='t'){
              printf("\n\nGacha Selesai Terima Kasih!\n\n");}
              else {
              printf("\n\nMaaf Format Salah");}



              return 0;

          }
