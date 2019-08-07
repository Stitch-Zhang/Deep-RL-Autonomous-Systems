# Ideas

This is a collection of ideas born from readings of articles on the web or personal speculations during sleepless nights.

## The Track

The design and training of a good driving model cannot go beyond the construction and design of a good track, 
especially as regards the training phase. For this reason I would like to redesign the track following the following
ideas and weaknesses:

- **Reflection on the track**: The track must be made from material with **low light reflection**. Therefore the circuit must be
enclosed by a sort of **wall**, high enough to block the light that could reflect anyway.

- **Lane dimensions and design**: In order to better simulate the spaces of a road environment, it would be better to plan the road
taking into account the relationships between the dimensions of the vehicle and the dimensions of the lane.
On average the cars are about 160/170 cm large, while the lane is between 275cm and 375cm. Our Cozmo is just 5.5cm wide,
which results in a ratio of about 1/30. The lane could therefore have dimensions between **9 cm** and **12.5cm**.
 The lane must be well delimited by strips of color in contrast to the color of the asphalt.
We can therefore use a white parcel tape large enough to be well detected by the Cozmo camera.

- **Avoid distractions**: Cozmo learns through a camera through a model-free algorithm that is not based on models inserted
as input to the problem. This can then lead him to learn anything in an uncontrolled way: maybe he could learn something
from the chairs in the background or from the shoes of the people walking.
In order to reduce this problem we could insert a margin between the road and the end of the carpet, but, above all, 
insert a wall at the end of it that could allow Cozmo, at least in the phase of its training, to focus on the lane.


### Useful Links
- [Build Your Track AWS DeepRacer](https://docs.aws.amazon.com/deepracer/latest/developerguide/deepracer-build-your-track.html)
- [LinkedIn Article about DeepRacer](https://www.linkedin.com/pulse/ive-students-meet-aws-deepracer-wong-chun-yin-cyrus-%E9%BB%83%E4%BF%8A%E5%BD%A5-/)

## Simulator

I think it may be useful to spend a few days looking for a simple and fastest method to design a simple simulator. The simulator will have to provide a  simple landscape with colours similar to those from the physical path.

Acceleration should be a value between `[0,1]` while steering between `[-1, 1]`. It would also be interesting to automate the car's exit from the road, starting a new episode from the beginning.

It would be useful to validate and test the values of hyper-parameters before proceeding with the experiment physically.

I will try crash courses to see if it could be feasible with Unity.