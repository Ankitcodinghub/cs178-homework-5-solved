# cs178-homework-5-solved
**TO GET THIS SOLUTION VISIT:** [CS178 Homework 5 Solved](https://www.ankitcodinghub.com/product/cs178-homework-5-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90969&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS178 Homework 5 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
&nbsp;

Problem 1: Clustering

In this problem, you will experiment with two clustering algorithms implemented in the updated mltools package: k-means and agglomerative clustering.

<ol>
<li>Load the standard Iris dataset, select the first two features, and ignore the class (or target) variables. Plot the data and see for yourself how “clustered” you think it looks. Include the plot, say how many clusters you think exist, and briefly explain why. (There are multiple reasonable answers to this question.) (5 points)</li>
<li>Run k-means on the first two features of the Iris data, for k = 2, k = 5, and k = 20. Try multiple (at least 5) different initializations for each k, and check to see whether they find the same solution; if not, pick the one with the best score. For the best clustering for each candidate k, create a plot with the data colored by assignment, and the cluster centers. You can plot the points colored by cluster assignments z using
ml.plotClassify2D(None,X,z) . (You will need to also plot the cluster centers yourself.) (15 points)
</li>
<li>Run agglomerative clustering on the first two features of the Iris data, first using single linkage and then again using complete linkage, using the algorithms implemented in ml.cluster.agglomerative from cluster.py ). For each linkage criterion, plot the data colored by their assignments to 2, 5, and 20 clusters. (Agglomerative clustering does not require an initialization, so there is no need to run methods multiple
times.)
</li>
</ol>
4. Briefly discuss similarities and differences in the outputs of the agglomerative clustering and k-means

algorithms.

Problem 2: EigenFaces

In class, we discussed how PCA has been applied to faces, and showed some example results. Here, you’ll explore this representation yourself. First, load the data and display a few faces to better understand the data format:

1 2 3 4 5

</div>
</div>
<div class="layoutArea">
<div class="column">
X = np.genfromtxt(“data/faces.txt”, delimiter=None) # load face dataset

plt.figure()

# pick a data point i for display

img = np.reshape(X[i,:],(24,24)) # convert vectorized data to 24×24 image patches plt.imshow( img.T , cmap=”gray”,vmin=0,vmax=255) # display image patch; you may have to

􏰀→ squint

</div>
</div>
<div class="layoutArea">
<div class="column">
<ol>
<li>Subtract the mean of the face images (X0 = X − μ) to make your data zero-mean. (The mean should be of the same dimension as a face, 576 pixels.) Plot the mean face as an image. (5 points)</li>
<li>Use scipy.linalg.svd to take the SVD of the data, so that X0 =U·diag(S)·Vh
Since the number of faces is larger than the dimension of each face, there are at most 576 non-zero singular values; use the full_matrices=False argument to avoid using a lot of memory. As in the slides, then compute W = U.dot( np.diag(S) ) so that X0 ≈ W · Vh. Print the shapes of W and Vh. (10 points)
</li>
</ol>
</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
</td>
</tr>
</tbody>
</table>
</div>
<div class="page" title="Page 2">
<table>
<tbody>
<tr>
<td></td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
3. For K = 1,…,10, compute the approximation to X0 given by the first K eigenvectors (or eigenfaces): Xˆ0 = W[:,: K] · Vh[: K,:]. For each K, compute the mean squared error in the SVD’s approximation,

np.mean( (X0 − Xˆ0)**2 ) . Plot these MSE values as a function of K. (10 points)

4. Display the first three principal directions of the data, by computing μ+α V[j,:] and μ-α V[j,:], where α is a scale factor (we suggest setting α to 2*np.median(np.abs(W[:,j])) , to match the scale of the data). These should be vectors of length 242 = 576, so you can reshape them and view them as “face images” just like the original data. They should be similar to the images in lecture. (10 points)

5. Choose any two faces and reconstruct them using the first K principal directions, for K = 5, 10, 50, 100. Plot the reconstructed faces as images. (5 points)

6. Methods like PCA are often called “latent space” methods, as the coefficients can be interpreted as a new geometric space in which the data are represented. To visualize this, choose 25 of the faces, and display them as images with the coordinates given by their coefficients on the first two principal components:

1 2 3 4 5 6 7 8 9

10 11

This plot is a good way to gain intuition for what the PCA latent representation captures. (10 points) Problem 3: Statement of Collaboration (5 points)

It is mandatory to include a Statement of Collaboration in each submission, that follows the guidelines below. Include the names of everyone involved in the discussions (especially in-person ones), and what was discussed.

All students are required to follow the academic honesty guidelines posted on the course website. For programming assignments in particular, I encourage students to organize (perhaps using Piazza) to discuss the task descriptions, requirements, possible bugs in the support code, and the relevant technical content before they start working on it. However, you should not discuss the specific solutions, and as a guiding principle, you are not allowed to take anything written or drawn away from these discussions (no photographs of the blackboard, written notes, referring to Piazza, etc.). Especially after you have started working on the assignment, try to restrict the discussion to Piazza as much as possible, so that there is no doubt as to the extent of your collaboration.

Problem 4: Course Evaluation

What were your favorite parts of CS178, and what machine learning topics do you wish you had learned more about? Please complete the official UC Irvine course evaluation to let us know. (You do not need to include any answer to this question in your submission; we will automatically determine which students complete the evaluation. Note also that we do not have access to the evaluation scores submitted by individual students; we can only see aggregate statistics of these scores.)

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
idx = … # pick some data (randomly or otherwise); an array of integer indices

import mltools.transforms

coord,params = ml.transforms.rescale( W[:,0:2] ) # normalize scale of “W” locations

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
plt.figure(); for i in idx:

# compute where to place image (scaled W values) &amp; size

loc = (coord[i,0],coord[i,0]+0.5, coord[i,1],coord[i,1]+0.5)

img = np.reshape( X[i,:], (24,24) ) # reshape to square

plt.imshow( img.T , cmap=”gray”, extent=loc, vmin=0,vmax=255 ) # draw each image

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
plt.axis( (-2,2,-2,2) ) # set axis to a reasonable scale

</div>
</div>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td></td>
</tr>
</tbody>
</table>
</div>
