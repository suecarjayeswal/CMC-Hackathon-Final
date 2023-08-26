# Simplified House Addressing
This repo contains the KUCMC CodeWare project of Team S.A.S.
Team nepalensis is a team of three delegates Swikar Jaiswal, Arnav Khadka, and Sabal Humagain. The team had been formed to participate in
KUCMC CodeWare Hackathon, organized by **[KUCMC (Kathmandu University Computational Mathematics Club)](https://cmclub.ku.edu.np/)**. It was a 24 hour hackathon venued at GolGhar, KU central campus, Dhulikhel.
We'd like to thank KUCMC club and mentors from **[Naxa](https://naxa.com.np/)** also, **[Naxa](https://naxa.com.np/)** and **[Itonics](https://www.itonics-innovation.com/)** for the insightful workshops

# Hackathon's Project Problem:
Two Billion people around the world do not have their own Physical Address. A family residing in a remote hill doesn't have proper address as that of family residing in a village or near any proper landmark. We need a physical addressing system/algorithm which is:
* Intuitive and easy to understand to layman
* Computationally efficient
* Interpolable, two addresses can be used to guess 3rd address
* Wary of privacy and security concerns i.e. confidential detail shouldn't be used


# Our Solution:
We have thought of a really simle and intuitive home addressing system. It is targeted to entities that need to account Details of houses/buildings in a certain region.
Take following two cases:
        *(Imagine you have a register of houses with details about their orders. If you are identifying each house by owner's name or any serial ID, comparing two IDS won't tell you about their proximity or such geo information.
        Using Lat-Lon as index is not intuitive but more prone to error.)
        *(Addressing a House by street name, doesn't inform exactly which house on the street)
        *(Addressing A house based on multiple landmarks for accuracy is neither sustainable nor computationally efficient. You will have to recalculate everything and make changes to database if landmark is removed.)

## We propose following model for house addressing:
1. The business or the concerned entity will be chosen as reference or will choose a reference.
2. Then vertical and horizontal lines with respect to North-East will be drawn in desired gap-width.
3. Each line will have a serial encoding. (eg: A,B,C for horizontal and 1,2,3 for vertical lines.)
4. Since any building will cross multiples, we will take two extreme horizontal and vertical lines for addressing.
5. Eg: A house crosses lines D,E,F,G and 6,7,8 then its address will be "DG-6-8"
6. This addressing system can accomodate for Apartments as well by adding one more hyphen to depict to 'storeys' eg.: DG-6-8-2 for 2nd floor

## Advantages of this system:
1. Two houses having similar or close letters/numbers means they are close. **Intuitive**
2. Eg.: DG-2-3 and BG-9-9 will be on same line i.e G line.
3. Addressing new buildings will only require what grids they occupy. **Sustainable**
4. Addressing houses in a given region will require small computation and only once. **computationally efficient**
5. No Collisions in Addresses
6. Tallying no of buildings will be much easier.

Screenshots:



### Note:
The notebook present in the Repo uses DBSCAN for Adaptive Grid making. This is computationally inefficient and really unneccessary for our purpose as such grids aren't sustainable. While the final result in it is evident that one house address can be used to speculate address of other house.

## Relevant Photos:
![Demo](/Data/teamSAS.gif)


GitHub Accounts:
* [**@arnav-khadka**](https://github.com/Arnav-Khadka)
* [**@sabal77**](https://github.com/sabal77)
