# ClassifyingRetinalOCTImages
 Classifying Retinal OCT images with CNNs using Keras in Python.
 
 Optical Coherence Tomography: Clinical Applications

Optical coherence tomography (OCT) is a techinque developed in 1991 for imaging retina, the photosensitive layer of the eye. It uses a non-invasive light beam and derives an image of the target tissue (e.g., retina, anterior chamber...etc.) using low-coherence interferometry to generate cross-sectional images in-vivo! There are many uses for OCT which revolve around inspecting abnormalities within these ocular tissues. For instance, the very high resolutions (of upto 5 microns from a Fourier Domain OCT) can be used to evaluate the integrity of anterior chamber, retinal thickness, neurosensory as well as blood capillary complexes (RPE-Choroid complex) in great detail. A few (from a long list of) tissue abnormalities that can be picked up by an OCT scan with high confidence include -

a. Epiretinal membranes

b. Macular holes (Pseudo and otherwise)

c. Subretinal fluid

d. Neurosensory detachments

e. Pigment-epithelial detachments

f. Choroidal neovascular membranes (CNV)

g. Age Related Macular Disease related irregularities in RPE.

For a more detailed description, you can check out this webpage hosted at Ophthalmic Photographer's Society.

In the Current Dataset, we are going to inspect 4 classes of these Retinal OCT images

We have a set of 84,495 images that include 4 groups of images in our current dataset.

Normal (label: NORMAL) - This class of data includes images of retina that show all the retinal layers intact, a clear vitreo-retinal interface, posterior hyaloid, normal foveal pit.

Choroidal Neovascularization (label: CNV) - CNV is a sign noted in exudative age-related macular degeneration (AMD) that typically involves an abnormal growth of new blood vessels (hence the name neovascularization) from the choroidal vasculature. In doing so, it threatens the patient's vision by obscuring and damaging the neurosensory retina.

Diabetic Macular (O)edema (label: DME) - DME is an accumulation of fluid (edema or known as 'swelling') involving the hydro-ionic homeostasis in the retinal blood barrier. This disruption is caused due to Diabetis and acts a marker in diagnosing diabetic retinal diseases.

Drusen (label: DRUSEN) - Drusen are yellow colored lipid deposits under the retina associated with Age related Macular Degeneration (AMD). There are various sizes and shapes of Drusens. However, in our dataset, we group them all under a single label.

Please visit this useful resource if you would like to know more about OCT and its utility and the specific ways in which OCT of retinal images can be read or understood.

A side-by-side comparision of our classes

![OCT IMAGES](https://els-jbs-prod-cdn.literatumonline.com/cms/attachment/4d0da5d1-ed26-4571-bc3f-8d1b02af390b/gr2.jpg)

@IMAGE COURTESY: http://www.cell.com/cell/fulltext/S0092-8674(18)30154-5

The data is organized into 3 folders (train, test, and val), each with 4 subfolders representing our classes (NORMAL, CNV, DME, DRUSEN).

Each image is labeled as (class)-(randomID)-(imageIDfortherandomID).

Our goal is to predict the class that each image belongs to (and therefore, the condition associated with the image) using neural nets that are optimized for speed if possible.

Let's inspect our data, preprocess it, balance our classes as needed, and then build some predictive models
