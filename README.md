# Smart India Hackathon Workshop

**Date:** 14.11.2025
**Register Number:** 212223040021
**Name:** Ashwin Kumar A

---

## Problem Title

**SIH 1555:** Create a Virtual Herbal Garden that provides an interactive, educational, and immersive experience to users, showcasing the diverse range of medicinal plants used in AYUSH (Ayurveda, Yoga & Naturopathy, Unani, Siddha, and Homeopathy).

## Problem Description

**Background:** The AYUSH sector relies heavily on medicinal plants and herbs, which form the backbone of traditional healing practices. However, physical gardens are not accessible to everyone. A Virtual Herbal Garden will bridge this gap by offering a digital platform where users can explore, learn, and understand the significance of various medicinal plants from the comfort of their homes.

**Description:** Participants are tasked with developing a Virtual Herbal Garden that is engaging, informative, and user-friendly. This virtual garden should include:
* **Interactive 3D Models:** Realistic 3D models of medicinal plants that users can rotate, zoom, and explore from different angles.
* **Detailed Information:** Comprehensive details about each plant, including its botanical name, common names, habitat, medicinal uses, and methods of cultivation.
* **Multimedia Integration:** High-quality images, videos, and audio descriptions to enhance the learning experience.
* **Search and Filter Options:** Advanced search functionality to easily locate specific plants and filter them based on various criteria like medicinal uses, region, and type.
* **Virtual Tours:** Guided virtual tours highlighting specific themes, such as plants for digestive health, immunity, skin care, etc.
* **User Interaction:** Features that allow users to bookmark favourite plants, take notes, and share information on social media.

**Expected Outcome:** The expected outcome is a comprehensive Virtual Herbal Garden that serves as a valuable educational tool for students, practitioners, and enthusiasts of the AYUSH sector. This platform should make the knowledge of medicinal plants accessible to a wider audience, promoting awareness and understanding of traditional herbal practices. It should be visually appealing, informative, and interactive, providing users with an immersive experience that combines technology with traditional knowledge.

## Problem Creater's Organization

Ministry of AYUSH

## Idea

Our solution, the **"AYUSH Digital Flora"**, is an immersive, AI-enhanced, and cross-platform virtual garden. It goes beyond a simple 3D library by integrating Augmented Reality, a gamified learning experience, and an AI "Virtual Vaidya" (healer) to guide users.

1.  **Immersive AR (Augmented Reality) Mode:** Users can select a plant from the 3D library and project it into their own environment using their mobile camera. This allows them to see the plant's scale and details in their own home or garden, making the experience highly interactive and memorable.
2.  **AI-Powered "Virtual Vaidya" Chatbot:** An AI assistant, trained exclusively on the verified AYUSH database, will guide users. Users can ask questions like, "Which plants are recommended for immunity?" and the chatbot will provide information and link directly to the relevant plants and virtual tours.
3.  **Gamified Thematic Tours:** Virtual tours will be structured as interactive "quests" or "trails" (e.g., "The Digestive Health Trail"). Users can earn badges for completing tours, correctly identifying plants in a quiz, or finding plants mentioned by the AI Vaidya.
4.  **Personal "My Garden" Dashboard:** A personalized space where users can bookmark (or "plant") their favorite herbs. This dashboard also saves all their notes, quiz scores, and bookmarked videos in one place.
5.  **Multi-Language Audio Support:** To ensure accessibility, all plant descriptions and tour guides will feature audio narration in multiple Indian regional languages, not just English and Hindi.
6.  **High-Fidelity 3D Models:** We will use photogrammetry to create highly realistic 3D models from actual medicinal plants, ensuring botanical accuracy.

## Proposed Solution / Architecture Diagram

The solution is a scalable, 3-tier cloud-native application designed for high availability and rich media streaming.

1.  **Frontend (Client-Side):** A cross-platform mobile application built using **Unity** or **React Native / Flutter** to handle AR functionality (via ARCore/ARKit) and 3D rendering. A parallel **Web App (React.js + Three.js/Babylon.js)** will provide access via browsers using WebGL.
2.  **Backend (Server-Side):** A microservices architecture using **Node.js (Express)** or **Python (Django)**. This will include:
    * **Main API:** Handles user authentication, plant data retrieval, notes, and bookmarking.
    * **Chatbot Service:** A separate Python service using a **RAG (Retrieval-Augmented Generation)** model (like LlamaIndex/LangChain) that connects to a vector database of AYUSH knowledge.
    * **Search Service:** Powered by **Elasticsearch** for fast and complex filtering (by use, region, name, etc.).
3.  **Database (Data Layer):**
    * **PostgreSQL:** For structured data (user profiles, plant metadata, notes, quiz results).
    * **Amazon S3 / Azure Blob Storage:** For storing large multimedia assets (3D models, high-res images, videos, audio files).
    * **Vector Database (e.g., Chroma/Pinecone):** To store the AYUSH knowledge base for the AI chatbot.

Here is a conceptual diagram illustrating the architecture:

http://googleusercontent.com/image_generation_content/0



---

## Use Cases

Our platform is designed for a diverse set of users, each with unique needs and interactions.

1.  **AYUSH Student:** A BAMS (Bachelor of Ayurvedic Medicine and Surgery) student uses the app to study. They use the advanced search to filter plants by their botanical names, view 3D models to study their morphology, and use the AR feature to compare digital models to real-world samples. They take extensive notes in the "My Garden" dashboard for exam preparation.
2.  **General Enthusiast:** A user interested in traditional remedies asks the "Virtual Vaidya" chatbot, "What plants are good for a cold?" The bot suggests the "Respiratory Health" tour and links to the 3D models for Tulsi, Ginger, and Pepper. The user takes the gamified tour and bookmarks the plants.
3.  **AYUSH Practitioner:** A Siddha doctor uses the app on a tablet to educate a patient. They pull up the 3D model of a specific herb, rotate it to show the roots and leaves, and play the audio description of its uses, helping the patient understand their prescription better.
4.  **Tourist or Researcher:** A researcher or tourist visiting a physical herbal garden (which may have limited signage) can use a (future) "image recognition" feature to scan a real plant, identify it, and instantly pull up its 3D model and data from the app.

Here is a Use Case Diagram for the AYUSH Digital Flora:

http://googleusercontent.com/image_generation_content/1



## Technology Stack

* **Frontend (Mobile):** **Unity** (for C# and robust 3D/AR) or **React Native** (for cross-platform JS)
* **Frontend (Web):** **React.js** (or Vue.js)
* **3D/AR Rendering:** **Three.js** (Web), **ARKit/ARCore** (Mobile), **Unity AR Foundation**
* **Backend:** **Node.js (Express.js)**, **Python (Django / Flask)**
* **AI/Chatbot:** **Python**, **LangChain / LlamaIndex**, **RAG Pipeline**
* **Database:** **PostgreSQL** (Relational), **Amazon S3** (Object Storage), **Chroma DB** (Vector DB)
* **Search:** **Elasticsearch**
* **3D Modeling Tools:** **Blender**, **Meshroom** (Photogrammetry)
* **Deployment:** **Docker**, **Kubernetes**, **AWS / Azure / GCP**

## Dependencies

* **1. Data Collation & Verification (Critical):** Sourcing and digitizing comprehensive, accurate medicinal data from the Ministry of AYUSH and other verified botanical sources.
    * *Time Estimate:* 12-16 weeks
* **2. 3D Model Creation:** Creating a large library (100+ plants) of high-fidelity, botanically accurate 3D models.
    * *Time Estimate:* 16-20 weeks
* **3. AI Chatbot Knowledge Base:** Curation and cleaning of the text-based knowledge to train the RAG model and prevent hallucinations.
    * *Time Estimate:* 8 weeks
* **4. AR Module Optimization:** Ensuring the AR feature works smoothly across a wide range of mid-to-low-end devices.
    * *Time Estimate:* 6 weeks
* **Estimated Budget:** Rs. 8,00,000 - 12,00,000 (To cover 3D modeling contracts, cloud infrastructure costs, and AI service integration).
