# 📘 R-SIT Ontology

### *Robotic Social Interaction Taxonomy*

R-SIT is a lightweight ontology for describing **social situations**, **agents**, **environments**, and **interaction dynamics**.
It is designed for social scene understanding, dataset annotation, and human–robot interaction research.

---

## 🧩 1. Core Concepts

R-SIT models three main types of entities:

* **SocialSituation** – the social scene or event
* **Agent** – any human participant
* **Location** – where the situation occurs

These are grouped under the generic class **RSITEntity**.

---

## 🎛️ 2. Dimensions

Dimensions describe attributes of situations, agents, and environments.

### **Environment Dimensions**

* **PhysicalEnvironmentType:** `Indoor`, `Outdoor`
* **Formality:** `Formal`, `Informal`

### **Situation Dimensions**

* **Cardinality:** `Solo`, `Dyad_1to1`, `Triad_1to2`, `SmallGroup_N`
* **CrowdContext:** `Crowded`, `NotCrowded`
* **SocialRelationType:** `PeerRelation`, `StrangerRelation`, `AdultChildRelation`
* **InteractionType:**

  * Goal-directed: `Cooperative`, `Competitive`, `Persuasive`
  * Norm-conformity: `Conforming`, `Observational`
* **CommunicationMode:** `Verbal`, `Nonverbal`
* **InterdependenceLevel:** `HighInterdependence`, `LowInterdependence`
* **NonverbalCue:** `ProximityClose`, `ProximityFar`, `EyeContact`, `BodyOrientation`
* **EmotionalValence:** `Positive`, `Neutral`, `Negative`
* **EngagementLevel:** uses ORO individuals (`engaged`, `engaging`, `disengaging`)

### **Agent Dimensions**

* **SocialRole:** e.g., `PeerPeerRole`, `StrangerStrangerRole`
* **SocialHierarchy:** `Dominant`, `Equal`, `Submissive`

---

## 🏠 3. Environment Instances

Concrete places are modeled as **individuals**, not classes:

* `KitchenEnvironment`
* `CafeteriaEnvironment`
* `LivingRoomEnvironment`
* `CoworkingSpaceEnvironment`
* `OfficeRoomEnvironment`
* `MeetingRoomEnvironment`
* `HospitalOfficeEnvironment`
* `StreetSidewalkEnvironment`
* `PublicParkEnvironment`

Each is annotated with:

```ttl
:hasPhysicalType Indoor/Outdoor
:hasFormality Formal/Informal
```

---

## 🔗 4. Key Object Properties

* `hasLocation`
* `hasPhysicalType`
* `hasFormality`
* `hasCardinality`
* `hasCrowdContext`
* `hasInteractionType`
* `hasCommunicationMode`
* `hasInterdependenceLevel`
* `hasNonverbalCue`
* `hasEmotionalValence`
* `hasEngagementLevel`
* `hasSocialRole`
* `hasHierarchyStatus`

---

## 📌 5. Example Annotation

```ttl
:Situation_Example a :SocialSituation ;
    :hasLocation :CafeteriaEnvironment ;
    :hasCardinality :Triad_1to2 ;
    :hasInteractionType :CooperativeInteraction ;
    :hasCommunicationMode :NonverbalCommunication ;
    :hasNonverbalCue :ProximityClose ;
    :hasEmotionalValence :PositiveValence ;
    :hasEngagementLevel oro:engaged .
```

---

## 🔖 **How to Cite R-SIT**

```bibtex
@misc{pallonetto2025rsit,
  title={R-SIT: Robotic Social Interaction Taxonomy},
  author={Pallonetto, Luca and Lemaignan, Severin},
  year={2025},
  publisher={GitHub},
  howpublished={\url{https://github.com/lulilac/R-SIT}}
}
```


