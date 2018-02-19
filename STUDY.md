https://github.com/googlecartographer/cartographer_ros/issues/264

Hi, I have uploaded my configurations ( I have changed then around a bunch of different ways kinda trial and error). Any advice you can provide would be awesome.

I put the files up on github at: https://github.com/nobertgmuedu/gmukitti

We are using Kitti Dataset, with Cartographer ROS. I am using a modified kitti2bag to convert the kitti datafiles to bag files (provided on github). It basically adds compression setting, ditches the images, and also ditches the TF frame, which allows me to configure robot with URDF instead. I hosted a bag file on amazon S3 at https://s3.amazonaws.com/kittigmu/kitti_2011_10_03_drive_0027_synced.bag .

Obviously the launch files, configurations, etc are all on github as well, should be ready to run with minimal if any hassle.

Here is a quick overview of the route, https://github.com/nobertgmuedu/gmukitti/blob/master/kitti_2011_10_03_drive_0027_synced.png there should be 5 loop closures (i marked green, purple, blue, red, and yellow) and near the end it pretty much totally gets lost running in circles. To be fair I think this is one of the most complex Kitti files in their entire dataset. The black arrows are where the car "should" be traveling, instead of the big loop you see it doing at the end.

This is the same dataset that the asset writing it crashing on too. With the smaller resolution it does better on some of the loop closure, like the blue dots "nearly" touch.

Lastly, here is a youtube video of the same dataset being navigated with other software for comparison sakes: https://www.youtube.com/watch?v=KYvOqUB_odg

Anyways, any feedback/suggestions on getting KITTI working better with Cartographer are more than welcome.

Thanks!

-Nathan


https://www.youtube.com/watch?v=KYvOqUB_odg

ICP-Based Pose-Graph SLAM
