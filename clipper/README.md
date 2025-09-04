
1. download

   `get_iplayer --type radio https://www.bbc.co.uk/sounds/play/m002hv3b`

2. clip

   `ffmpeg -i "World_at_One_-_Angela_Rayner_admits_not_paying_enough_stamp_duty._m002hv3b_original.m4a" -ss 40:37 -to 41:12 -c copy "2025-09-03-World_at_One_40-37_to_41-12.m4a"`

3. merge audio and still image

   `ffmpeg -loop 1 -i ~/Downloads/chris-pattan.jpg -i ~/2025-09-03-World_at_One_40-36_to_41-12.m4a -c:v libx264 -tune stillimage -c:a aac -b:a 192k -pix_fmt yuv420p -shortest out.mp4`


