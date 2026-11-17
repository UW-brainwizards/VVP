# USE CASE 1:: VIEW MRI AND MRE BRAIN IMAGES

### Who is the User?
* **Persona/Role:** 
Johnny (Neuroscience MS student)
Sofia (Neuroscience student)
Charlie (Medical student)
Sarah (Medical student)
Shanae (ME student)
Marcus (Undergrad) 
Isabelle (High school student)

* **Context:** Users with little to no coding experience who want to explore brain imaging data visually and learn about brain anatomy and imaging modalities

### What Do They Want to Do with the Tool?
* **Primary Tasks:**
  * Load and display MRI and MRE brain scans
  * Browse through anatomical slices
  * View labeled brain structures
* **Operational Workflows:**
  * User selects a sample dataset or uploads their own scan
  * Tool renders the brain image slice by slice
  * User toggles anatomical labels on/off

### What Are the Inputs and Outputs?
* **Inputs:** Sample or uploaded brain imaging data (MRI or MRE)
* **Outputs:** Rendered brain images with optional anatomical labels and explanatory tooltips

### What Are Their Needs and Desires?
* Plain-language explanations of what they are seeing
* Intuitive navigation requiring no coding
* Labeled anatomical structures
* Side-by-side MRI and MRE views

### What is Their Skill Level?
* Beginner to intermediate; little or no programming, imaging, or ML experience

### Implied Use Cases
* The tool must silently handle NIfTI or similar file formats in the background — most users will never think about file formats but the tool cannot work without this
* A sample dataset must always be available so users without their own data can still explore

---

# USE CASE 2: GENERATE AND VIEW MODEL PREDICTIONS

### Who is the User?
* **Persona/Role:** 
Sandi (ME MS student)
Kate (ML grad student)
Melinda (Math grad student)
Jordan (Data science student)
Dr. Patel (Biomedical imaging researcher)
Daniel (Research assistant)

* **Context:** Users with some technical background who want to run the deep learning model on MRI inputs and see the resulting predicted stiffness map

### What Do They Want to Do with the Tool?
* **Primary Tasks:**
  * Select or upload an MRI input
  * Run the deep learning model
  * Display the predicted MRE stiffness map
* **Operational Workflows:**
  * User selects a sample or uploads their own MRI scan
  * Tool runs the model and returns a predicted stiffness map
  * Predicted map is rendered as a heatmap alongside the MRI input

### What Are the Inputs and Outputs?
* **Inputs:** MRI scan (uploaded or selected from sample dataset)
* **Outputs:** Predicted MRE stiffness map rendered as a heatmap

### What Are Their Needs and Desires?
* Fast and reliable prediction
* Clear visual output with a labeled color scale
* Step-by-step explanation of what the model is doing (for less experienced users)
* Information about model limitations and what predictions should not be used for

### What is Their Skill Level?
* Intermediate to advanced; comfortable with Python and data analysis, varying ML and MRI experience

### Implied Use Cases
* The tool must handle prediction failures gracefully with clear error messages (bad input format, missing data, incompatible dimensions) — essential but easily overlooked
* The tool must clearly communicate that predictions are not clinical diagnoses

---

# USE CASE 3: COMPARE PREDICTED VS REFERENCE STIFFNESS MAPS

### Who is the User?
* **Persona/Role:** 
Kate (ML grad student)
Jordan (Data science student)
Leo (ML student)
Dr. Patel (Biomedical imaging researcher)
Melinda (Math grad student)

* **Context:** Users who want to assess how closely the model's predictions match the ground truth MRE maps

### What Do They Want to Do with the Tool?
* **Primary Tasks:**
  * Display predicted and reference maps side by side
  * View a difference/error map highlighting where predictions deviate
  * Inspect specific regions of interest
* **Operational Workflows:**
  * User selects a subject with both a predicted and reference map available
  * Tool renders both maps side by side with a consistent color scale
  * Tool generates an error map showing the difference

### What Are the Inputs and Outputs?
* **Inputs:** Predicted stiffness map + reference MRE map for the same subject
* **Outputs:** Side-by-side visualization, error/difference map, optional region-level statistics

### What Are Their Needs and Desires?
* Consistent color scale across both maps so comparison is meaningful
* Ability to zoom into specific brain regions
* Downloadable visualizations for reports and presentations

### What is Their Skill Level?
* Intermediate to advanced; comfortable with data visualization and ML metrics

### Implied Use Cases
* A consistent color scale across predicted and reference maps is implied but critical — without it the comparison is misleading
* The tool must clearly label which map is predicted and which is reference to avoid confusion

---

# USE CASE 4: EVALUATE MODEL PERFORMANCE

### Who is the User?
* **Persona/Role:** 
Kate (ML grad student)
Dr. Patel (Biomedical imaging researcher)
Jordan (Data science student)
Raj (ML engineer)
Daniel (Research assistant)
Leo (ML student)

* **Context:** Users who want to systematically assess how well the model performs across a dataset, not just on a single sample

### What Do They Want to Do with the Tool?
* **Primary Tasks:**
  * View performance metrics (MAE, MSE, SSIM) per subject and in aggregate
  * Browse results across multiple subjects
  * Identify cases where the model performs poorly
* **Operational Workflows:**
  * User navigates to a performance dashboard
  * Tool displays summary statistics and per-subject breakdowns
  * User filters or sorts by metric to find edge cases

### What Are the Inputs and Outputs?
* **Inputs:** Prediction results across a dataset with corresponding reference maps
* **Outputs:** Performance summary table, per-subject metrics, error visualizations, downloadable results

### What Are Their Needs and Desires?
* Transparent and consistent performance summaries
* Ability to identify cases associated with poor image quality or specific tissue regions
* Downloadable results for use in research discussions and reports
* Documentation of training data and known model limitations

### What is Their Skill Level?
* Intermediate to advanced; comfortable with statistics, ML metrics, and data analysis

### Implied Use Cases
* Downloading results as a CSV or image file is implied by the research context even if not always explicitly stated
* Performance must be broken down by subject, not just reported as a single aggregate number, to be useful for researchers

---

# USE CASE 5: EXPLORE EDUCATIONAL CONTENT ABOUT MRI AND MRE

### Who is the User?
* **Persona/Role:** 
Priya (Curious student)
Isabelle (High school student)
Fatima (Science communicator)
Carmen (Museum exhibit designer)
Lena (Physical therapist) 
Sarah (Medical student)
Charlie (Medical student)
Shanae (ME student)

* **Context:** Users with no or limited technical background who want to understand the biological, physical, and technical concepts behind brain stiffness mapping and AI prediction

### What Do They Want to Do with the Tool?
* **Primary Tasks:**
  * Read plain-language explanations of MRI, MRE, and brain stiffness
  * View labeled visual examples
  * Follow a guided walkthrough of the prediction process
* **Operational Workflows:**
  * User lands on an educational section of the site
  * They read explanations and explore labeled diagrams and example images
  * They follow guided examples without needing to write any code

### What Are the Inputs and Outputs?
* **Inputs:** None — static educational content
* **Outputs:** Educational pages with text, diagrams, labeled brain images, and guided examples

### What Are Their Needs and Desires?
* Plain-language explanations with no assumed technical knowledge
* Visual demonstrations that work without code
* Guided examples that connect MRI inputs to stiffness map outputs conceptually
* Context about why brain stiffness matters clinically and scientifically

### What is Their Skill Level?
* Beginner; little or no programming, neuroscience, or ML experience

### Implied Use Cases
* This content must be fully accessible without login or technical setup
* The educational section must load quickly and work on mobile devices since not all users will be at a research workstation