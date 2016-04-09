#Jibo Orbiting Eye demo

This comes from a discussion on the Jibo Developer forum at https://discuss.jibo.com/t/orbiting-jibo-eye-animation/739 (At the moment you have to be an early access developer to access this, I believe.)

Timothy created an animation to orbit Jibo's eye, and provided the formulas and values, but was hand-jamming them into the Animation editor.

This skill is a demo of how to calculate the values to save yourself some typing.

The master branch precomputes an orbit and stores the necessary values in an array, then plays these values back to produce the orbit.

The real-time branch computes these values at each step of the animation based on the previous values. It is more labor-intensive, but would be more useful if you were going to change some of the basic parameters during the orbit. (Like move the center, or speed it up or something.)

This is example code, and isn't directly useful for anything. It could also certainly be improved.

One last note: because of a current SDK bug that evaulates a TimeoutJS expression at the beginning of the behavior tree, I had to move the TimeoutJS into a Subtree and pass the delay in as a parameter to that tree. Once the SDK bug is fixed this will probably just be a simple TimeoutJS behavior. 
