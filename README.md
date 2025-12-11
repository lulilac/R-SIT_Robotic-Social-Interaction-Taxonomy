# 📘 R-SIT Ontology

### *Robotic Social Interaction Taxonomy*

R-SIT is a lightweight ontology for representing **social situations**, **agents**, **environments**, and **interaction dynamics**.
It is designed for social scene understanding, dataset annotation, and human–robot interaction research.

---

## 🧩 1. Core Entities

These classes represent the *things that exist* in a social scene:

* **SocialSituation** – the social event or context
* **Agent** – any human participant
* **Environment / Location** – the place where the situation occurs

All core entities descend from **RSITEntity**.

---

## 🎛️ 2. Dimensions

Dimensions describe properties of situations, locations, and agents.
Each dimension is independent, allowing flexible annotation.

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
* **EngagementLevel:** reuses ORO individuals (`engaged`, `engaging`, `disengaging`)

### **Agent Dimensions**

* **SocialRole:** `PeerPeerRole`, `MasterSlaveRole`, `StrangerStrangerRole`
* **SocialHierarchy:** `Dominant`, `Equal`, `Submissive`

---

## 🏠 3. Environment Instances

R-SIT includes concrete **Location individuals** for common settings:

* `KitchenEnvironment`
* `LivingRoomEnvironment`
* `CafeteriaEnvironment`
* `CoworkingSpaceEnvironment`
* `OfficeRoomEnvironment`
* `MeetingRoomEnvironment`
* `HospitalOfficeEnvironment`
* `StreetSidewalkEnvironment`
* `PublicParkEnvironment`

Each location is annotated with:

```ttl
:hasPhysicalType Indoor/Outdoor
:hasFormality Formal/Informal
```

---

## 🔗 4. Key Object Properties

Relations used to describe a social situation:

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


