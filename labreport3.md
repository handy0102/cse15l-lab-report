# Lab Report 3

I'll be using the **grep** command :D.

All my examples came from https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix

## grep -r "string" file-name/directory
**EX1)**

Input:
`
andyho@Andys-MacBook-Air Abernathy % grep -r "In the late 1940s"`

Output:
`./ch1.txt:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.`

Explanation:
This command takes in the string pattern "In the late 1940s". It then recursively searches in the current directory (Abernathy) and its subdirectories for exact matches and outputs the lines that contain the match along with the file name. This is useful for looking for specific data inside big data files. 

**EX2)** 

Input: 
`andyho@Andys-MacBook-Air written_2 % grep -r "no matching string"`

Output:
No output :(

Explanation:
This command takes in the string pattern "no matching string". It searches for a line with the matching string, but it does not find any. This is useful for checking if specific patterns exist in a data file.

## grep -c "string" file-name

**EX1)**

Input: 
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Bahamas" Bahamas-History.txt`

Output:
`23`

Explanation:
This command takes in a string pattern "Bahamas" and returns the number of lines that contain that string inside Bahams-History.txt. This command is useful for checking if the string pattern is a common occurance in a text file.

**EX2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Not Bahamas" Bahamas-History.txt`

Output:
`0`

Explanation:
Takes in the string "Not Bahamas" and counts the number of lines that pattern appears. In this case it's zero, because no line in that file contains it. This is useful for confirming if there is no sentence/word that appears in the text file.

## grep -v "string" file-name

**EX1)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -v "Bahamas" Bahamas-history.txt` 

Output:
`A Brief History
Colonization and Piracy
In 1670 six Lords Proprietors of Carolina were granted the Bahama islands by Charles II, but for nearly 50 years their weak governors on New Providence either couldn’t or wouldn’t suppress the piracy raging through the archipelago. Then, in 1684, to avenge countless raids against their ships, the Spanish dispatched a powerful squadron from Cuba to attack Nassau. This sent the majority of the English settlers fleeing to Jamaica or Massachusetts, but didn’t have much effect on the pirates.
New Providence knew some spells of prosperity in the mid-18th century as privateering resumed with England at war with Spain. The town of Nassau expanded, and improvements were made between 1760 and 1768 by another revered governor, William Shirley from Massachusetts.
The American Revolutionary War
Emancipation and Decline
Nassau became a free port in 1787, sparking a surge in trading activity. Loyalists built a number of the attractive colonial-style homes and public buildings still standing today, and during the War of 1812, privateers enjoyed another profitable spell against American vessels.
Civil War Blockade Running
For a time a new fiber called sisal seemed promising. But Bahamian soil was too poor and Mexico grew a better plant. Neville Chamberlain, future British Prime Minister, took over his family’s sisal operation on Andros in the 1890s. It failed, the natives said, because of that island’s evil elves called chickcharnies, who cast a spell on the family for disturbing the land. Hopes were raised, and also fizzled, over Bahamian citrus and pineapple. Sponging, another vitally important industry at the end of the 19th century, also had setbacks. A hurricane in 1839 drowned some 300 sponge fishermen in the ‘mud’ off Andros, and a devastating fungus some 40 years later killed almost all the sponges.
The 20th Century
Desperate for work, perhaps 20 percent of the Bahamian population left to take construction jobs in Florida between the turn of the century and World War I. During that war hundreds of Bahamians saw active service with British forces. The islands suffered food shortages and a serious bank failure, but nothing more threatening militarily than rumors of German submarines offshore.
Liquor money bought Nassau better houses, churches, lighting, water, roads, sewers, docks, and hotels. The city’s first gambling casino opened in 1920; the first daily air service from Miami began in 1929; the yacht set decided Nassau was fashionable, and many wealthy Americans as well as Prohibition millionaires built homes on the islands.
Then, to the astonishment of the local populace, the Duke of Windsor, having given up his throne for an American divorcée, was named governor of the little colony in 1940. He and the Duchess remained until 1945.`

Explanation:
This command basically returns all the lines from Bahamas-History.txt that don't contain the string "Bahamas". This is really useful for people who are allergic to the word "Bahamas", but still want to read an article on the Bahamas. Idk maybe Sam Bankman stole their money.

**EX2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -v -i "surf" bali-whattodo.txt`

Output:
`What to Do
Sports
At the top of the list of Bali’s great attractions are its beaches with the warm waters of the Indian Ocean lapping at the shores, but the range of active and sports choices is hardly limited to floating on the waves. The more unusual spectator sports include colorful water buffalo races (on Lombok) and, to the horror of many visitors, cockfighting, a local favorite on both Bali and Lombok, where it is sometimes carried on as part of religious ceremonies or festivals.
Watersports
Warm water, gorgeous coral, and vivid fish make for great snorkeling over the reefs, especially off the north coast of Bali, Nusa Lembongan, and Lombok’s offshore Gilis (see page 74). Take your own equipment if you have it. Otherwise, many hotels will lend or rent it to you — check the fit and condition carefully. Superb sites for SCUBA diving include Menjangan and Nusa Penida off Bali, and the Gilis. Specialist tour operators rent out all the equipment and run courses for complete beginners — make sure that the company you choose is licensed and that the instructors are fully qualified, with international certification.
Most resorts give you a number of swimming options. When the tide or sea conditions don’t suit, there is usually a pool. If there isn’t one where you are staying, you may be able to use another hotel’s pool for a small charge.
Whitewater rafting is one of the newer activities. Tour companies will pick you up at your hotel, then take you to the launch point on the Ayung river near Ubud, and provide you with the necessary equipment for an exhilarating trip. 
On Dry Land
Golf courses at Nusa Dua and up in the mountains at the Bali Handara Kosaido Country Club are both top-class, staging tournaments which bring some of the world’s best players. There’s a 9-hole course at Sanur, and at Lombok there is the 18-hole Suranadi course. Many hotels offer their own tennis courts, some floodlit for evening use. Air-conditioned squash courts are available at a few places. As the sun starts to set, informal soccer and volleyball games between visitors and locals begin on the beach at Kuta, Tuban, and Legian.
Walking in the countryside is one of the great pleasures of Bali. Don’t start at the southern resorts, which are a long way from the best scenery, but begin instead up in the hills, where it’s cooler. In Ubud, the Bina Wisata Information Center or your hotel can give you information on walks along the Campuan Ridge, or through picturesque local rice fields. Bookstores in Ubud sell detailed maps, including Bali Pathfinder and Ubud Surroundings, that will help guide you along country pathways. Keep Walking Tours (<balitrade@denpasar.wasantara.net.id>) at the Tegun Galeri shop in Jalan Hanoman offers one- to seven-hour guided walks; Victor Mason’s highly praised Bali Bird Walks (Tel. 0361 975 009) includes lunch, water, and use of binoculars. Both are very reasonably priced. At Munduk, in the beautiful mountains southwest of Lovina, Puri Lumbung Cottages (see page 134) offers an excellent program of walks, treks, and courses in local arts and crafts.
More arduous and serious mountain treks include climbing the active volcano Gunung Batur — a trek of several hours — and the crater rim and lake of Gunung Rinjani (on Lombok), which demands at least three days to complete.
Massage, both relaxing and therapeutic, is a Balinese tradition that many visitors have come to enjoy. The beaches are filled with men and women offering reasonably good massage at prices that are very low. Ubud has many good massage centers that offer very professional massage treatment, including mineral baths, all for approximately US$10; hotels and resorts offer similar treatment in more pampering surroundings for considerably more.
Spectator Sports
Regular buffalo races are held at Negara in western Bali, and on Lombok, with the normally sluggish beasts pulling decorated carts at surprising speeds. Kite-flying is a local obsession at Sanur and on the windswept Bukit Peninsula. You can buy beautiful, hand-painted kites at stands or from hawkers at Sanur and also at Kuta.
In Lombok, ritual fights long ago took the place of war. The Balinese and Sasaks hurl packets of cooked rice at each other in the October perang ketupet festival. Large crowds gather regularly in villages in Lombok to watch peresehan contests in which men armed with rattan canes and leather shields lash at each other until the referee declares one of them the victor.
Entertainment
Traditional Music, Puppetry, and Dance Performances
The sound of music in Bali can be the hypnotic tones of the gamelan orchestra, or the alluring call of the disco beat at Kuta or Legian, where the action begins at midnight and lasts until dawn. In the rest of the resorts, the nightlife is on a much smaller scale.
Bali’s own celebrated culture of dance and drama flourishes on two levels: for the visitors and for locals themselves. Ask at hotels, travel agencies, and tourist information offices to find out what is scheduled during your stay. They’ll probably point you towards some of the commercial performances put on in several villages, mostly in the Ubud area. Tickets (including transport) are sold at the tourist office in Ubud and by many of the tour operators. Increasingly, the culture is packaged and brought to you in shows staged at hotels. Some of these are of a very high standard: Dedicated dancers and musicians usually do give their best. But inevitably the atmosphere is different when they are performing for untutored tourists eating dinner, rather than for an expert village audience — and above all for their gods.
Drama and dance students will think that they’ve gone to heaven when they see the unique temple ceremonies. If you are invited, be prepared to wait for a long time. Starting times are highly elastic, and then some events will last for many hours. 
Many of the dances of Bali are also performed in western Lombok, either for the Balinese community there or, increasingly, for the tourists at Senggigi hotels. Lombok also has its own special dances, which are rarely staged commercially. Some are for men only — one simulating battle preparations probably derives from the Islamic tradition. The gandrung dance closely resembles Bali’s joged, in that a girl picks a male partner from the audience. Another group of dances is based on romantic legends from Sasak mythology, dating back to before the advent of Islam. Western-style nightlife is limited to Senggigi, where some hotels run discos and local groups play in the bar-restaurants.
The puppet shadow plays called wayang kulit (leather puppet) are not so often put on for tourists — the plots are too complex and the plays last too long (up to two days) for foreign consumption. A temple ceremony may give you a chance to join the audience for a while. You may look behind the screen — it’s permitted — to see the dalang or puppet master expertly controlling the beautiful figures, speaking all of their lines in a vast range of appropriate voices while conducting the small orchestra.
Dances of Bali
Legong: This is the visitors’ favorite dance, performed by three young girls: two principal dancers, the legongs, no more than 12 or 13 years old, and an attendant. Each is exquisitely dressed in glittering songket fabrics and wears a gilded and jeweled head-dress embellished with fresh frangipani (plumeria) flowers. The usual version (legong kraton) is the tale of a king and the princess he has abducted, performed by the two principals who, using various hand and facial gestures, portray the attempted seduction. 
Kecak: Part of a much longer ritual trance-dance which is called sanghyang, this is mostly performed separately. Up to 150 men in sarongs crouch in concentric circles around a flickering lamp and chant hypnotically while the story is acted out in the center of the circle. Taken from the Ramayana, the dance concerns Rama and Sita and the monkey armies of Hanuman and Sugriwa, hence the kecak’s popular title of “Monkey Dance.” The dance as performed today was choreographed by the German artist, Walter Spies, who did so much to influence art in the Ubud region during the 1930s.
Pendet: Six or more girls carrying trays of flower petals open the evening by scattering the petals over the stage as a symbol of welcome. At the same time, a man may light an incense-burning lamp. At temple ceremonies the pendet is danced to welcome the gods.
Janger: Twelve boys and twelve girls in groups of six form a square, the girls kneeling and swaying together to the music like reeds in the wind. The boys, wearing false moustaches, try to impress the girls as they strut and preen like fighting roosters.
Joged: A whole family of dances shares this name, performed to the music of an orchestra of bamboo xylophones and gongs. But one, properly called the jegog, has become so popular that it alone is often considered to be joged. A young woman dances alone at first, and then taps members of the audience in turn to dance with her. Try as they may to flirt or show off, she easily slips away from their advances. Few Westerners look anything but clumsy in comparison.
Barong: A mythical lion-like animal, the barong is covered in long hair and little mirrors. Animated by two men, it fights against the evil Rangda, queen of the witches. Her long claw-like fingernails hold a white cloth to hide her terrible face, bulging eyes, fangs, and flaming tongue while she advances on her victims. Allies of the barong, men wearing sarongs and each carrying a kris, try to attack Rangda but she puts them under a spell. In a trance, they turn the knives on themselves. Only the reappearance of the barong saves them.
In daily performances for visitors (each morning at Batubulan, for instance) the trances are inevitably simulated. Late at night in a village, however, you would see the wild-eyed men in a genuine frenzy or collapsing at the climax into unconsciousness, until revived by priests who sprinkle them with holy water.
Other Dances: Other performances you might see include scenes from the Hindu epic drama, the Ramayana, staged as a ballet. These may well be a showcase for fine dancing, gorgeous costumes, and the full range of the gamelan orchestra. In the topeng, the dancers are masked, meaning that they can convey character and emotion through movement alone. The stories are taken from Balinese history and mythology. 
Kebyar is the name of a group of solo dances of which the best known are performed by a seated man, using only the upper body. Baris is a vehicle for groups of young male dancers to display their command of technique, conveying a great range of emotions.
Festivals and Events
Most festivals are fixed by calendars different from the Western version (see page 91), so they change each year. Look for the Indonesian Directorate of Tourism’s annual Calendar of Events, which is published in Bali and gives dates and locations of temple festivals. Two celebrations stick to fixed dates: The Walter Spies festival in February and the summer Arts Festival, with superb performances, which is held in Denpasar in late June and early July.
Shopping
Bali produces a wide range and large quantity of crafts in every medium. Most of the decorative arts and crafts originally had a religious connection, as temple embellishments, offerings, or ceremonial dress. The land yielded plenty to eat without the need to work all day, every day, so people had time to create objects of beauty. The tradition continues, although production has been multiplied by the demand for souvenirs. Some craft shops in the villages have workshops attached, or you can watch the carvers, painters, or weavers in the adjoining compound.
In the past, nothing was expected to last: The climate and insects saw to that. So hardly anything is very old — “Antiques Made to Order” shop signs give the game away. 
Wood carvings: Dozens of villages devote themselves to Bali’s biggest craft business; Mas (see page 41) is the best-known, with hundreds of carvers and countless shops. Behind the scenes — but you may be invited for a visit — fathers pass on their skills to their sons, while the women do the polishing or painting. The best carvings are superb sculptures, but even the simplest, cheapest article can make an appealing souvenir. Among the massed garuda birds and masks, you’re bound to find something beautiful. 
The sign “Parasite Carvings” might puzzle you. A new idea, imported from the West, is to take the galls and other strange growths that occur on tree trunks and carve them into a witty or grotesque design, using the natural shape.
Jewelry: The village of Celuk (see page 40) specialized in producing silver and gold jewelry for centuries, so when tourism arrived, its position on the Denpasar-Ubud road was ideal. Dozens of tour buses stop at the big shops but there are many little workshops worth visiting, too. The smiths can produce any style: from intricate filigree work to simple bracelets. You don’t have to go to Celuk though, since every resort area has its share of shops. Silver should bear the “925” stamp of sterling silver (meaning it’s 92.5% pure).
Clothes and Fabrics: Bali is a huge bargain basement for a selection of beachwear, casual clothing, and, at a higher price but still excellent value, fashion designs. For the biggest choice of shops go to Kuta, and look for dresses, shirts, sarongs, and cover-ups in traditional batik fabric. 
Batik dyeing technique uses hot wax to draw or stamp a design on cloth before dipping it in the dye, so that the waxed areas are left undyed. The process can be repeated a number of times for greater complexity. Java is the source of the batik for dresses and sarongs sold in fashion shops; Balinese versions are usually much coarser. Hawkers will swear that their dress lengths of cheap printed cotton are batik. It’s easy to tell that they are not: Printed patterns don’t penetrate fully to the other side, while the real batik will show thin veins of color where the dye runs along tiny cracks in the wax (printed versions may try to simulate this). Real batik is always much more expensive. Used batik sarongs are highly prized, as their patterns are often no longer produced. Used batik can be bought for very low fixed prices at textile shops like Alec, on Jalan Legian in Kuta-Legian.
Endek or ikat fabrics, using threads dyed in patterns before weaving, come from Gianyar in Bali as well as other Indonesian islands. In Bali, only the weavers of Tenganan make grinsing, or double ikat, using pattern-dyed threads for both warp and weft. The genuine fabric is justifiably expensive — beware of fakes! You can find bold, primitive examples of ikat cloth, especially from islands such as Sumba, Flores, and Timor, in good textile shops.
Paintings: If you want a unique work of art, you’ll need to study the field. Visit the major collections to judge the standard of the best paintings, especially the Neka Museum and Museum Puri Lukisan in Ubud (see page 41) as well as the Arts Centre in Denpasar (see page 37). Don’t just assume that a high price guarantees original work.
And More… Look for the basketry from Bona, leather wayang kulit puppets from Puaya near Sukawati, and decorative umbrellas on roadside stalls east of Klungkung.
Shops take advantage of the tourist traffic to sell the products of other islands, too — embroidery and songket fabrics from Sumatra, primitive art from Irian Jaya, and silver from Sulawesi.
Lombok: Craft skills in Lombok tend to be devoted to household objects that can have a somewhat austere functional beauty. Look for the delicate, tightly-woven basketware, whether in mats, boxes, bowls, and bags, or the common Lombok souvenir of a model rice-barn. Painted wood boxes to store spices, tobacco, or jewelry are attractive. Simple red pottery comes from Penujak, and black pots from Rungkang are bound in an intricately woven basket.
Necessities: Some supermarkets and convenience stores have opened in Denpasar, such as Tiara Dewata, on Jalan Jenderal Sutoyo, with books, shoes, cosmetics, and even a playground for children and a swimming pool. There is a similar big shopping center near the airport, while smaller ones can be found in Kuta, Nusa Dua, Senggigi, and Lombok. In big towns, modern grocery shops, with big red “K” signs (Circle K) are open 24 hours a day and sell all kinds of necessities.
Bali FORCHILDREN
The Balinese treasure their children and yours will get the same treatment. Some resorts run children’s activity programs during the day, show videos in the early evening, and at night offer a babysitting service when you want to go off on your own. In losmen and homestay accommodations, the children of the owner’s family will probably want to make friends, and the older girls may offer to act as babysitters.`

Explanation:
Like example 1, it returns all the lines inside the inputted file that contain the inputted string. In this example, it helped me filter the lines with "surf" in it. I used -i so the captilization did not matter either. This command is useful for just filtering information that you find useless, like an activity that you've already done.


## grep --color "string" file-name

I don't think markdown supports different colors so I took screenshots of the output :).

Input:



