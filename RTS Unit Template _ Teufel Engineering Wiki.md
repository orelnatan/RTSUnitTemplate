9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

󰋜 / rts-unit-template 

## RTS Unit Template 

Copyright 2022 Silvan Teufel / <u>Teufel-Engineering.com</u> 󰏌 All Rights Reserved. 

# **RTS Unit Template - Readme - 2026** 

### **Create your own RTS Units !** 

- 

- 

- 

   - CTRL + E -- Rotate Cam Right (works also when Cam is locked to Unit ) 

   - CTRL + Q - Rotate Cam Left (works also when Cam is locked to Unit ) 

   - CTRL + Left Mouse Click -- Move Cam to Mouse Position 

- 

   - CTRL + W -- Zoom Cam In 

- 

   - CTRL + S -- Zoom Cam Out 

- 

   - CTRL + HOLD SPACE -- Fast Zoom Out to Position 

- 

   - CTRL + SPACE + Left Mouse - Move Cam to Mouse Position 

- 

- 

- 

   - Mouse to Screen Edges -- Move Cam to Mouse Position 

   - Right Click when Unit Selected -- Move Unit 

   - Shift + Right Click when Char. Sel. -- Move Unit through Waypoints 

- CTRL + G when Unit Selected -- Lock Unit on Character 

- 

   - CTRL + T when Unit Selected -- Switch to Third Person Mode 

- 

- 

   - Press A when Character Selected - toggle Attack 

   - Press A + Left Click when Character Selected - Move to Position and Attack 

- 

- 

- Press A + Left Click on Enemy - Focus this Enemy 

- HOLD TAB -- Show Control-Widget 

Gameplay Preview: https://youtu.be/FwVmgxJtab4 󰏌 

For Questions you can write to info@teufel-engineering.com or Join my Discord: <u>https://discord.gg/HM5f2zFazk 󰏌</u> 

If you find any Issues or Bugs i appreciate your Mail. I will fix any Bugs as soon as i can and update the Product. 

### **Download the Plugin** 

<u>https://www.unrealengine.com/marketplace/en-US/profile/Silvan+Teufel? count=20&sortBy=effectiveDate&sortDir=DESC&start=0 󰏌</u> 

https://wiki.teufel-engineering.com/en/rts-unit-template 

1/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

If you have downloaded the plugin it can be found in your Unreal Engine folder: C:\Program Files\Epic Games\UE_5.0\Engine\Plugins\RTSUnitTemplate (for example). or 

C:\Program Files\Epic Games\UE_5.0\Engine\Plugins\Marketplace\RTSUnitTemplate 

If you can find this folder in your enginge plugins folder the download was successful. If the plugin is in another folder, you should copy it here. 

### **Install the Plugin** 

Open Unreal Editor. Click Edit -> Plugins to open the plugin window. Search for RTSUnitTemplate and put a check mark at it. 

### **Import Settings** 

Check the Discord for newest Settings 

### **Enhanced Keyboard Settings** 

For using Enhanced Keyboard Settings the Plugin (Enhanced Input) has to be activated as well (from Unreal Engine). 

You can Change Inputs at: All\Engine\Plugins\TopDownRTSCamLib\Content\Blueprints\Controls 

For GameplayTags you have to set AssetMangerClass in ProjectSettings (Restart Project after change): 



<!-- Start of picture text -->
| Project Settings x EY Message Log # Plugin Untitled<br>hi seting X_AssetManager<br>bject Engine - General Settings<br><!-- End of picture text -->

Go to ProjectSettings->Input and set EnhancedIputComponentBase: 

https://wiki.teufel-engineering.com/en/rts-unit-template 

2/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
Engine - Input<br>af’ These settings are saved in Defaultinputini, which is currently writable<br>® Axi Action mag re now de} -d, please use EnhancedIr Actions and Ir ping Cor stead.<br>Viewport Properties<br>Input<br>He LegacyInput Scale<br>Fite input<br>4a Flush by PlatformPressed KeysUser on Focus L<br>Mobile<br>Virtua Keyboard (Mobile)<br>Defauit Classes<br>At PlayerInput Ca EnhancedPrayerinout v © RB<br>Default Input Component Class E InputCon wacv © BB<br><!-- End of picture text -->

YOu can set MappingContext and ControlAsset in the BP_CameraBase: 



<!-- Start of picture text -->
X  Mapr fa it<br>Top Down RTSCam Lib<br>MappingContext g2, — 'MC_Contr v<br>te 6<br>MappingPriority )<br><!-- End of picture text -->



<!-- Start of picture text -->
Input Bw<br>Input<br>ntrolAsset v<br>€B<br><!-- End of picture text -->

https://wiki.teufel-engineering.com/en/rts-unit-template 

3/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **Test Example Map** 

Open Unreal Editor. Open folder (In Unreal Editor folder tab): All\Engine\Plugins\RTSUnitTemplate\Content\RTSUnitTemplate\Level\levelOne 

### **Example Blueprints** 

Your can find example Blueprints in the Unreal Editor as well: All\Engine\Plugins\RTSUnitTemplate\Content\RTSUnitTemplate\Blueprints 

This Blueprints use the Parent Classes from RTSUnitTemplate Plugin, which you can use for your Blueprints. If you duplicate a Character make sure to reset the AttributeSet in the Details Panel of the Character/Unit BP. Otherwise Game will crash with this Character. 

### **Create a Blueprint from Parent Classes** 

1. Right Click inside the Content Browser inside the Unreal Editor -> Create Blueprint 

2. Go to "ALL CLASSES" Section and tipe the Name of the Parent Class inside the Search (Choose one of the ParentClasses) 

3. Click on Select 

4. Go in the Details Penal of you BP_Class and Type "RTSUnitTemplate" into the Search 

BP_UnitBase Setup 

1. For Character choose a Skeletal Mesh and a Animation Blueprint (there are Example Animation Blueprints in the Blueprint Folder 

All\Engine\Plugins\SwarmSimulator\Content\SwarmSimulator\Blueprints\Animations) 

2. Adapt the Trigger Capsule to the Mesh 

3. If you need a new Animation Blueprint for your Mesh Create it -> Right Click -> Animations -> Animation Blueprint 

4. Copy the Statemachine from my Example Animations Blueprints (All\Engine\Plugins\SwarmSimulator\Content\SwarmSimulator\Blueprints\Animations) 

5. Go through all States and change the Animation. 

6. Check if the Transition Rules are Setup Correctly. If not you can easily choose the right state from a dropdown. 

7. Check Details of the Blueprint by Typing SwarmSimulator in the Search. 

8. Use Functions and Variables in EvenGraph and Construction Script. Or just use the Parent Class as it is. 

9. Choose the AI Controller for the Unit 

#### BP_UnitBaseController 

1. When created the Blueprint u can just adapt the Details Panel by Typing in Search "RTSUnitTemplate" 

2. Choose the BP_UnitBaseController in your BP_UnitBase under "Ai Controller" 

Character Animation Statemachine 

https://wiki.teufel-engineering.com/en/rts-unit-template 

4/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. Right Click Create Animation -> Animation Blueprint 

2. Choose Parent Class of the CharacterBase -> CharacterBaseAnimInstance / EnemyBase -> EnemyBaseAnimInstance / MouseBotBase -> MouseBotBaseAnimInstance 

3. Choose Skeleton 

4. Copy Statemachine from 

   - (All\Engine\Plugins\SwarmSimulator\Content\SwarmSimulator\Blueprints\Animations) 

5. You can change the Time the Unit stuck in the Animation. This will also change Gameplay. To Adjust the Animation Times take a Look into the ControllerBase properties. 

#### HUD/Actor Setup 

1. Create a Blueprint like mentioned above. 

2. Type "RTSUnitTemplate" in Search Details. 

3. Use Functions and Variables in EvenGraph and Construction Script. Or just use the Parent Class as it is. 

#### Widget Setup 

1. Widgets have to be choosen inside the Blueprints of a Character 

2. Example Widgets are at 

   - (All\Engine\Plugins\RTSUnitTemplate\Content\RTSUnitTemplate\Blueprints\Widgets) 

3. Example Character with choosen Widgets can be found at 

   - (All\Engine\Plugins\RTSUnitTemplate\Content\RTSUnitTemplate\Blueprints\Character) 

4. Widget hast to been set Space "Screen" and Draw at Desired Size to true. (In the Widget and in the Character BP) 

5. Widget Class has to choose a Blueprint (in the Character BP). Or just use the Parent Class like it is. 

### **Setup your Animations.** 

1. Create a Blueprint from the AnimInstance 

https://wiki.teufel-engineering.com/en/rts-unit-template 

5/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
y1 Pick Parent Class x<br>COMMON<br>ro)<br>Qos An a is an object that can be placed or spawned in the<br>E Pawn fromA Pawnisa controlleran actor that can be ‘possessed’ and receive input ®<br>rc} arog phileaks ter is a type of Pawn that includes the ability to walk ®<br>#8 Player Controller APawnPlayer usedController4d byby 4 the playeris an, actor responsible for controlling~ a @@<br>& Game Mode Base defines the game being played, its rules<br>Game Mode Base scoring, and other facets of the game type<br>[I Actor Component added to any actor (0)<br>SESS ES transform and can be attached to other scene components @<br>ALL CLASSES<br>X  UnitBaseAnin °o4<br>@ Object<br>¢ Animinstance<br>© *% Une =einstance<br>Pal aUnitBaseAnimpscures<br>4 items (1 selected)<br>Select Cancel<br><!-- End of picture text -->

2. You have to create a Animation Blueprint 

https://wiki.teufel-engineering.com/en/rts-unit-template 

6/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
Animation ><br>_ Artificial Intelligence > py Aim Offset<br>Blueprints > 2%<br>( Cinematics > ot Animation Blueprint<br>Editor Utilities > .<br>Foliage > x Animation Composite<br>FX ><br>= Animation Layer Interface<br>a ameplay, ><br>MaterialsInputP >> aie. Animation Montage<br>ind<br>juste ” ¥ Blend Space<br>Miscellaneous > —<br>panerzb) 4 [at Mirror Data Table<br>Physics ><br>Sounds > Pose Asset<br>Textures ><br>User Interface > Advanced ><br>Control Rig ><br>IK Rig ><br>Legacy ><br><!-- End of picture text -->

3. Choose your Skeleton and my Class (preferbly as Blueprint) 

https://wiki.teufel-engineering.com/en/rts-unit-template 

7/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
Uw Create Animation Blueprint x<br>Specific Skeleton Template<br>Q fm<br>#H* Skeletor<br>+ Minion Lane_Siege_Skeleton<br>keleton<br>z Minion_Skeleton<br>s~_ — Prime_Helix_Skeletor<br>* _ Revenant_Skeleton<br>Z<br>mh<br>it SkeletoSK_M ene quin<br>16 items<br>Parent Class: BP_UnitBaseAniminstance_C<br>X BP_UNit it<br>7% Animinstance<br>~ UnitBaseAniminstance<br>4, DIT BaseAniminstance<br>3 items (1 selected)<br>Cancel<br><!-- End of picture text -->

4. Setting up a DataTable 

I have an Example DataTable. But the DataTable is Design for use with a 2D-Blendspace. 

Miscellaneous->DataTable 



<!-- Start of picture text -->
UW Pick Row Structure x<br>UnitAnimData v<br>OK Cancel<br><!-- End of picture text -->

DTUnitAnimData: 

https://wiki.teufel-engineering.com/en/rts-unit-template 

8/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
Row Name Anim State Blend Point 1 Blend Point2 Transition Rate 1 Transition Rate 2 Resolution? Resolution2 Sound<br>r I 5 75.000000 100000 1.000000 h<br>2<br>Run Run 75.000000 75.000000 5.000000 5.000000 5.000000 5.000000 None<br>3 Attack Attack 25.000000 25.000000 25.000000 25.000000 25.000000 25.000000 None<br>4 Pause Pause 0.000000 0.000000 000000 1.000000 1.000000 000000 None<br>5 Patrol Patrol 75.000000 75.000000 +~—1.000000 1.000000 1.000000 1.000000 _—None<br>6 Chase Chase 0.000000 50.000000 5.000000 5.000000 5.000000 5.000000 None<br>7 IsAttackec IsAttacked 75.000000  25.000000 5.000000 5.000000 5.000000 5.000000 ~—sNone<br>8 Dead Dead 100.000000 0.000000 1.000000 1.000000 1.000000 1.000000 —Non<br>9 Speaking Speaking 25.000000 50.000000 1.000000 1.000000 1.000000 1.000000 None<br><!-- End of picture text -->

The Table is chosen in the in Animation Blueprint: 



<!-- Start of picture text -->
Uy oO<br>B® w “8 ‘8 cs s > Sh " 2<br>:<br>a uf<br>¥ Rye<br>¥ ot<br>a<br>: speaking<br>sone > Beever} <> a<br>* Ss<br>ii , el|o<br>—<br>Ol»<br>sa {2 Customstateone .<br><!-- End of picture text -->

I have created example Blendspaces: 

https://wiki.teufel-engineering.com/en/rts-unit-template 

9/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
N (4 ®<br>1000 Hold Control to set the Preview Point (Green)<br>+ *<br>BlendPoint2 ¢:<br>ee —+<br>=<br>0.0 -— °<br>00 < BlendPoint 1.—> 1000<br><!-- End of picture text -->

And in the State General I use the Blendspace for all other States: 



<!-- Start of picture text -->
—— ee<br>Current Blend Point 1 a;BS_Wraith @)<br>BlendPoint Output Animation Pose<br>1 r == Wr Result<br>BlendPoint2<br>a .<br>Current Blend Point 2<br>++<br>—|<br>+++<br>——— °<br><!-- End of picture text -->

The StateMachine: 

https://wiki.teufel-engineering.com/en/rts-unit-template 

10/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 



<!-- Start of picture text -->
Entry D > Becenerat}] ——————> @ Speaking<br>@ CustomStateOne<br><!-- End of picture text -->

The Custom State can just be a Animation Output: 



<!-- Start of picture text -->
Recall<br>. Output Animation Pose<br>T So<br>. W- R ResultI<br><!-- End of picture text -->

# **Actors Technical Documentation** 

### **AWaypoint** 

1. **Purpose** : Core responsibility is acting as a world marker for unit movement, patrol paths, and characterfollowing logic. 

2. **Implementation (CPP Analysis)** : Logic in Tick manages a FollowTimerHandle which, via UpdatePositionToFollowCharacter , snaps the waypoint to a FollowCharacter 's 

location. OnPlayerEnter performs unit state validation, transitioning valid units into PatrolRandom or setting their next Waypoint and initiating Dijkstra pathfinding by setting DijkstraSetPath = true . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

11/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

3. **Blueprint Interface** : Includes NextWaypoint (AWaypoint*), FollowCharacter (AUnitBase*), and PatrolCloseToWaypoint (bool). Features UFUNCTIONs for UpdatePositionToFollowCharacter and OnPlayerEnter . 

4. **Component Architecture** : Setup in constructor with USceneComponent as root, UStaticMeshComponent (Mesh), UBoxComponent (Trigger Box), and UNiagaraComponent (Niagara_A). 

5. **Network/Replication** : Replicates Mesh , Niagara_A , TeamId , NextWaypoint , and FollowCharacter . Overrides IsNetRelevantFor to restrict visibility to the unit's own team or 

neutral markers. 

### **AMissile** 

1. **Purpose** : A lightweight projectile actor designed for simple linear movement and direct attribute damage application. 

2. **Implementation (CPP Analysis)** : Manual movement logic in Tick via SetActorLocation using Velocity * DeltaTime . OnOverlapBegin implements team filtering and checks for UnitData::Dead status; it applies damage by directly modifying unit attributes 

   - ( SetHealth_Implementation / SetShield_Implementation ) and signals the Mass system via UMassSignalSubsystem . 

3. **Blueprint Interface** : Exposes Mesh (UStaticMeshComponent), Velocity (FVector), Damage (float), and MaxLifeTime (float). 

4. **Component Architecture** : Rooted with a UStaticMeshComponent (Mesh) using the Trigger collision profile and overlap events enabled. 

5. **Network/Replication** : Basic actor replication enabled via bReplicates . 

### **AStoryTriggerActor** 

1. **Purpose** : Manages localized story events triggered by team-specific volume overlaps. 

2. **Implementation (CPP Analysis)** : BeginPlay fetches story data from a UDataTable ( FStoryWidgetTable ). OnOverlapBegin performs dual-gating: a team check for the triggering unit and a local player team check. If passed, it enqueues a FStoryQueueItem into the UStoryTriggerQueueSubsystem for sequential UI display. 

3. **Blueprint Interface** : StoryDataTable (UDataTable), StoryRowId (FName), and delegates OnStoryTriggered , OnStoryFinished . 

4. **Component Architecture** : UBoxComponent (TriggerBox) serves as the root and primary overlap volume. 

5. **Network/Replication** : bReplicates = true . Team filtering in OnOverlapBegin ensures the UI logic executes only for relevant clients. 

### **AFogActor** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

12/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Provides a client-side visualization of Fog of War using dynamic texture masking and postprocess materials. 

2. **Implementation (CPP Analysis)** : Creates a transient UTexture2D in InitFogMaskTexture . UpdateFogMaskWithCircles_Local (and multicast) implements a custom CPU-based drawing 

loop that converts world coordinates to pixel indices, drawing intensity circles into a TArray<FColor> buffer which is then uploaded via UpdateTextureRegions . 

3. **Blueprint Interface** : FogSize , FogTexSize , CircleRadius (int32), and FogUpdateRate (float). 

4. **Component Architecture** : UPostProcessComponent configured as bUnbound = true to apply the mask globally via a dynamic material instance. 

5. **Network/Replication** : Replicates TeamId , FogMinBounds , and FogMaxBounds . Circular reveal data is propagated via Unreliable multicasts. 

### **AAbilityIndicator** 

1. **Purpose** : Local-only visual placement guide for ability targeting and building construction. 

2. **Implementation (CPP Analysis)** : Caches OriginalMaterial on start. Handles visual validation by swapping materials when IsOverlappedWithNoBuildZone is true. Supports ResourcePlacementDistance checks to prevent placement near resource nodes. 

3. **Blueprint Interface** : IndicatorMesh (UStaticMeshComponent), 

   - DetectOverlapWithWorkArea (bool), and ResourcePlacementDistance (float). 

4. **Component Architecture** : USceneComponent root with an attached UStaticMeshComponent (IndicatorMesh) with collisions disabled. 

5. **Network/Replication** : bReplicates = false . Entirely client-side logic for the local player. 

### **AHealingActor** 

1. **Purpose** : Provides persistent, periodic area-of-effect healing to friendly units. 

2. **Implementation (CPP Analysis)** : Init applies an immediate MainHeal . Tick manages a ControlTimer to apply IntervalHeal every HealIntervalTime seconds to all units in 

the Actors array, up to MaxIntervals . 

3. **Blueprint Interface** : HealIntervalTime , MaxIntervals , IntervalHeal , and MainHeal . 

4. **Component Architecture** : UStaticMeshComponent (Mesh) as root and a UCapsuleComponent (TriggerCapsule) for unit registration. 

5. **Network/Replication** : Replicates Mesh and Material . Health modifications are authority-checked. 

### **AWorkArea** 

1. **Purpose** : Foundation for resource nodes and construction sites, managing building progression and worker limits. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

13/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : HandleBuildArea calculates build progress, updates CurrentBuildTime , and handles building/construction unit lifecycle. OnOverflowTimer is a 

looping check that uses SwitchEntityTagByState to return extra workers to base if they exceed MaxWorkerCount . 

3. **Blueprint Interface** : Type (WorkAreaType), ConstructionUnitClass , BuildTime , ConstructionCost (FBuildingCost), and MaxWorkerCount (int32). 

4. **Component Architecture** : Rooted with USceneComponent (SceneRoot) and an attached UStaticMeshComponent (Mesh) with customized collision responses for resource interaction. 

5. **Network/Replication** : Replicates Mesh , TeamId , Workers , BuildTime , CurrentBuildTime , and AvailableResourceAmount . 

### **AWorkResource** 

1. **Purpose** : Represents a resource asset attached to a unit's socket during gathering/return. 

2. **Implementation (CPP Analysis)** : SetResourceActive toggles mesh/material and visibility. OnRep_IsAttached and OnRep_ResourceType ensure that clients correctly render the 

specific resource type once assigned on the server. 

3. **Blueprint Interface** : ResourceMeshes / ResourceMaterials (TMaps), Amount , and SocketOffset . 

4. **Component Architecture** : UStaticMeshComponent (Mesh) as root. 

5. **Network/Replication** : Replicates Mesh , IsAttached , ResourceType , Amount , and SocketOffset . 

### **AProjectile** 

1. **Purpose** : Complex projectile handling linear, arced, and spiral homing flight paths with Mass integration. 

2. **Implementation (CPP Analysis)** : FlyInArc uses sinusoidal interpolation based on ArcTravelTime / TotalTravelTime . FlyToUnitTarget implements a spiral vector 

offset ( HomingOffset ) that varies over time. Multicast_UpdateISMTransform performs high-frequency synchronization of UInstancedStaticMeshComponent instances and Niagara transforms. 

3. **Blueprint Interface** : ArcHeight , HomingMissleCount , Damage , MovementSpeed , and ImpactVFX . 

4. **Component Architecture** : USceneComponent root, UInstancedStaticMeshComponent (ISMComponent) for optimized rendering, and dual UNiagaraComponent s for flight trails. 

5. **Network/Replication** : Extensive replication of flight parameters, targets, and visual states. 

### **AAutoCamWaypoint** 

1. **Purpose** : Trigger actor for automated camera movements or state changes in UIs/Controllers. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

14/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : Uses UBoxComponent overlap events to identify the local camera actor and trigger behavior defined in Blueprints. 

3. **Blueprint Interface** : Tag , NextWaypoint , OrbitTime . 

4. **Component Architecture** : USceneComponent (Root) and UBoxComponent (BoxComponent). 

5. **Network/Replication** : Replicates via reliable server function OnPlayerEnter . 

### **AEffectArea** 

1. **Purpose** : Zones that apply persistent UGameplayEffect s or modify unit visibility, supporting Mass Processor integration. 

2. **Implementation (CPP Analysis)** : ComputeLocalVisibility determines rendering based on local player team and FoW state. OnOverlapBegin applies AreaEffectOne/Two/Three to units via the Ability System Component. Integrates with Mass via UMassActorBindingComponent . 

3. **Blueprint Interface** : AreaEffectOne/Two/Three (UGameplayEffect classes), StartRadius , EndRadius , bIsInvisible . 

4. **Component Architecture** : USceneComponent , UInstancedStaticMeshComponent (ISMTemplate), UNiagaraComponent , and UMassActorBindingComponent . 

5. **Network/Replication** : Replicates effect definitions and visual trigger flags. 

### **ANoPathFindingArea** 

1. **Purpose** : Defines regions where pathfinding is obstructed or incurs high cost. 

2. **Implementation (CPP Analysis)** : Primarily acts as a spatial data container for navigation queries. 

3. **Blueprint Interface** : Radius (float). 

4. **Component Architecture** : Basic actor with no default components. 

5. **Network/Replication** : Standard actor replication. 

### **APickup** 

1. **Purpose** : Collectible actors that grant immediate rewards, effects, or abilities to units. 

2. **Implementation (CPP Analysis)** : Tick handles homing toward a unit once FollowTarget is active using UKismetMathLibrary::GetDirectionUnitVector . ImpactEvent triggers effect application via a switch on PickUpData::SelectableType . 

3. **Blueprint Interface** : Type (PickUpData), Amount , PickupEffect , and PickupAbility . 

4. **Component Architecture** : Root UCapsuleComponent (TriggerCapsule). 

5. **Network/Replication** : Replicates PickupEffect , TeamId , FollowTarget , and Target . 

### **ASaveGameActor** 

1. **Purpose** : World-space trigger for initiating the game saving/loading UI. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

15/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : OnOverlapBegin checks SelectableTeamId of the local controller and creates a USaveGameWidget . It uses bIsCameraMovementHaltedByUI to pause the camera. OnOverlapEnd sets a 5-second timer to cleanup the widget. 

3. **Blueprint Interface** : SaveGameWidgetClass , SaveSlotName . 

4. **Component Architecture** : UCapsuleComponent (OverlapCapsule) as root. 

5. **Network/Replication** : bReplicates = true . UI interaction is client-side. 

### **ADijkstraCenter** 

1. **Purpose** : Spatial reference actor for Dijkstra pathfinding algorithms. 

2. **Implementation (CPP Analysis)** : Minimalist marker used to define search origins in Dijkstra calculations. 

3. **Blueprint Interface** : Mesh and Material . 

4. **Component Architecture** : UStaticMeshComponent (Mesh). 

5. **Network/Replication** : Standard actor. 

### **UAreaDecalComponent** 

1. **Purpose** : Decal that supports time-based radius scaling and efficient Runtime Virtual Texture (RVT) writing. 

2. **Implementation (CPP Analysis)** : AdvanceMassScaling implements linear interpolation for the decal's radius. UpdateDecalVisuals manages a dynamic material for standard decals or configures a RVTWriterComponent (transient UStaticMeshComponent) to inject color and radius data into an RVT. 

3. **Blueprint Interface** : Server_ActivateDecal , Server_ScaleDecalToRadius , and RVT settings ( TargetVirtualTexture , RVTWriterMaterial ). 

4. **Component Architecture** : Subclass of UDecalComponent . 

5. **Network/Replication** : Replicates CurrentMaterial , CurrentDecalColor , CurrentDecalRadius , and bDecalIsVisible . 

### **AMapSwitchActor** 

1. **Purpose** : Level transition actor with orbital movement logic and minimap presence. 

2. **Implementation (CPP Analysis)** : Tick updates location using orbital math ( RotationRadius * Cos/Sin(CurrentAngle) ) around a CenterPoint . OnOverlapBegin enqueues the switch UI via UMapSwitchWidget . 

3. **Blueprint Interface** : TargetMap (SoftObjectPtr), SwitchTag , RotationSpeed , MarkerDisplayText . 

4. **Component Architecture** : UCapsuleComponent (OverlapCapsule) root and a UWidgetComponent (MarkerWidgetComponent). 

5. **Network/Replication** : Replicates orbital state and bIsEnabled . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

16/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **ARSVirtualTextureActor** 

1. **Purpose** : World manager for Runtime Virtual Textures, used for persistent AoE visuals. 

2. **Implementation (CPP Analysis)** : BeginPlay uses UGameplayStatics::GetAllActorsOfClass on ANavMeshBoundsVolume to 

aggregate total level bounds and scale the URuntimeVirtualTextureComponent accordingly. 

3. **Blueprint Interface** : bAutoSetBoundsFromNavMesh and VirtualTexture . 

4. **Component Architecture** : URuntimeVirtualTextureComponent (VirtualTextureComponent) root. 

5. **Network/Replication** : Standard actor. 

### **AMinimapActor** 

1. **Purpose** : Generates topography data via LineTraces and renders real-time unit position overlays. 

2. **Implementation (CPP Analysis)** : CaptureMapTopography iterates through a grid of LineTraces, sampling material parameters or SurfaceType to generate a static topography UTexture2D . Multicast_UpdateMinimap performs a high-speed CPU drawing pass for units and fog, then 

uploads to GPU. 

3. **Blueprint Interface** : MinimapBrightness , TagConfigs (TArray), FogOpacity . 

4. **Component Architecture** : UBoxComponent (MapBoundsComponent) defining the capture volume. 

5. **Network/Replication** : Replicates TeamId and bounds. Position data for units is updated via multicast. 

### **AMissileRain** 

1. **Purpose** : Spawns a designated number of AMissile actors over an area for area-denial effects. 

2. **Implementation (CPP Analysis)** : Tick manages a timed spawner loop using RainTime . It calculates random locations within MissileRange and uses BeginDeferredActorSpawnFromClass to instantiate missiles. 

3. **Blueprint Interface** : MissileCount , MissileRange , MissileBaseClass . 

4. **Component Architecture** : UStaticMeshComponent (Mesh) root. 

5. **Network/Replication** : Server-side spawning logic. 

### **USelectionDecalComponent** 

1. **Purpose** : Component for rendering unit selection circles. 

2. **Implementation (CPP Analysis)** : Directly configures its orientation and size in the constructor. ShowSelection creates/updates a UMaterialInstanceDynamic to set the SelectionColor parameter. 

3. **Blueprint Interface** : SelectionColor , ShowSelection , HideSelection . 

4. **Component Architecture** : Subclass of UDecalComponent . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

17/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Local visual component. 

### **AUnitSpawnPlatform** 

1. **Purpose** : Production building that manages unit positioning, slot-based spawning, and energy accumulation. 

2. **Implementation (CPP Analysis)** : UpdateUnitPositions ensures produced units stay aligned on the mesh using FQuat::RotateVector . ReSpawnUnits checks SpawnedUnits and replenishes empty slots using SpawnUnit (deferred spawning) if energy is available. 

3. **Blueprint Interface** : DefaultUnitBaseClass , Energy , MaxEnergy , UnitSpacing . 

4. **Component Architecture** : UStaticMeshComponent (PlatformMesh), USceneComponent (SpawnPoint), and UWidgetComponent (EnergyWidgetComp). 

5. **Network/Replication** : Replicates Energy , MaxEnergy , and TeamId . 

### **ASelectionCircleActor** 

1. **Purpose** : High-performance selection indicator manager using a single shared plane and opacity mask. 

2. **Implementation (CPP Analysis)** : Multicast_UpdateSelectionCircles renders sharp 1-pixel square outlines into a transient UTexture2D based on unit positions. The material on the CircleMesh samples this texture as an opacity mask to show indicators for many units 

simultaneously. 

3. **Blueprint Interface** : CircleMapSize , CircleTexSize , SelectionCircleUpdateRate . 

4. **Component Architecture** : UStaticMeshComponent (CircleMesh) as root. 

5. **Network/Replication** : TeamId replicated. Mask updates via Unreliable multicasts. 

### **AEnergyWall** 

1. **Purpose** : Connects buildings with a traverse-blocking energy shield and dynamic navigation obstacle. 

2. **Implementation (CPP Analysis)** : UpdateWallTransformAndDimensions positions rod and shield ISMs between two ABuildingBase actors. RegisterObstacle calculates NavObstacleBox extents and uses UNavigationSystemV1::AddDirtyArea to mark 

NavMesh regions for re-baking. 

3. **Blueprint Interface** : DespawnDelay , FriendlyEffectClass , InitializationDuration . 

4. **Component Architecture** : USceneComponent (WallRoot), UInstancedStaticMeshComponent (Top/Bottom Rods, Shield), UBoxComponent 

(NavObstacleBox), UNavModifierComponent . 

5. **Network/Replication** : Replicates connected building references and bIsDeactivated state. 

### **AWinLoseConfigActor** 

1. **Purpose** : Centralized actor for defining, tracking, and progressing through mission-specific objectives. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

18/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : AdvanceToNextWinCondition manages the objective lifecycle. OnRep_TagProgress synchronizes the count of alive units/buildings matching specific gameplay 

tags with the UI. 

3. **Blueprint Interface** : WinConditions (TArray), LoseCondition (EWinLoseCondition), and victory/defeat delegates. 

4. **Component Architecture** : Logic-only actor with no visual components. 

5. **Network/Replication** : Replicates current objective index, condition data, and progress metrics. 

### **AIndicatorActor** 

1. **Purpose** : Floating world-space indicator for displaying numbers (damage/healing). 

2. **Implementation (CPP Analysis)** : Tick applies random drift and vertical movement over its MaxLifeTime . Multicast_UpdateWidget retrieves the UDamageIndicator widget 

from the component to set its numeric and color state. 

3. **Blueprint Interface** : DamageIndicatorComp , LastDamage , ZDrift . 

4. **Component Architecture** : UWidgetComponent (DamageIndicatorComp) as root. 

5. **Network/Replication** : Multicast_UpdateWidget synchronizes the numeric value and colors across clients. 

# **Animations Module Technical Documentation** 

### **FUnitAnimData** 

1. **Purpose** : Defines a data structure for animation configuration rows within a Data Table, mapping unit states to specific animation parameters. 

2. **Implementation (CPP Analysis)** : Inherits from FTableRowBase for Unreal Engine DataTable compatibility. It stores UnitData::EState as a lookup key and provides target values for blend spaces ( BlendPoint_1 , BlendPoint_2 ), interpolation speeds ( TransitionRate_1 , TransitionRate_2 ), and precision thresholds ( Resolution_1 , Resolution_2 ). It also 

associates a USoundBase asset with the state. 

3. **Blueprint Interface** : All members are exposed via UPROPERTY(EditAnywhere, BlueprintReadWrite, Category = RTSUnitTemplate) , allowing designers to define animation behavior in the Editor's DataTable spreadsheet. 

4. **Component Architecture** : Uses GENERATED_BODY() macro. No specialized constructor logic is present as it is a data-only structure. 

5. **Network/Replication** : Not directly replicated. This struct is used to populate UUnitBaseAnimInstance properties which are themselves replicated. 

### **UUnitBaseAnimInstance** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

19/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : The core Animation Instance class responsible for driving character animations based on the AUnitBase state, handling smooth parameter transitions, and state-triggered audio. 

2. **Implementation (CPP Analysis)** : 

   - NativeUpdateAnimation : Polls the AUnitBase owner to synchronize CharAnimState . It manages a SoundTimer to trigger UGameplayStatics::PlaySoundAtLocation exactly once when entering a state (if a 

   - sound is defined). It performs manual linear interpolation for CurrentBlendPoint_1 and CurrentBlendPoint_2 : if the absolute difference between the current and target value is within 

   - the Resolution threshold, it snaps to the target; otherwise, it moves by the TransitionRate . 

   - SetBlendPoints : Iterates through the AnimDataTable to find a matching state row. It 

   - includes specialized logic for ASpeakingUnit , checking the SpeechBubble animation time to determine if it should use speech-specific blend points or revert to the default state data. 

3. **Blueprint Interface** : 

   - UPROPERTY members like CharAnimState , CurrentBlendPoint_1 , and CurrentBlendPoint_2 are available for access within Animation Blueprints (AnimBP). 

   - SetBlendPoints is a BlueprintCallable function allowing manual updates to the 

   - animation targets. 

   - AnimDataTable is a configurable UDataTable reference for defining the unit's animation 

   - profile. 

4. **Component Architecture** : The constructor initializes CharAnimState to UnitData::Idle . It overrides NativeInitializeAnimation and NativeUpdateAnimation . 

5. **Network/Replication** : Implements robust multiplayer support via 

   - GetLifetimeReplicatedProps . It uses DOREPLIFETIME for almost all internal state and 

   - transition variables, including CharAnimState , BlendPoints , TransitionRates , Sound , and SoundTimer , ensuring that animation states and smooth transitions are synchronized 

   - from the server to all clients. 

### **UStoryBlueprintLibrary** 

1. **Purpose** : 

A static Blueprint Function Library acting as the primary entry point for the Story System. It facilitates the creation and queuing of story-driven UI elements (widgets) by interfacing with the UStoryTriggerQueueSubsystem . 

2. **Implementation (CPP Analysis)** : 

- **Subsystem Interaction** : All functions retrieve the UStoryTriggerQueueSubsystem from the UGameInstance via WorldContextObject->GetWorld()->GetGameInstance() . 

- **Data Encapsulation** : Functions convert individual parameters or DataTable row data into a FStoryQueueItem struct before passing it to the subsystem's EnqueueStory method. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

20/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ 

   - **EnqueueStory** : Handles hard-referenced assets ( UTexture2D* , UMaterialInterface* ). 

- **EnqueueStorySoft** : Handles soft-referenced assets ( TSoftObjectPtr ), reducing immediate memory pressure and cook-time dependencies. 

- **EnqueueFromDataTableRow** : Uses Table->FindRow<FStoryWidgetTable> to pull structured data from a UDataTable . Implements a random selection fallback using FMath::RandRange on Table->GetRowNames() if the provided RowName is empty and bRandomIfNone is 

- enabled. 

#### 3. **Blueprint Interface** : 

- EnqueueStory : UFUNCTION(BlueprintCallable, Category="Story") . Takes hard 

- references to UI assets, text, and sound. 

- EnqueueStorySoft : UFUNCTION(BlueprintCallable, Category="Story") . 

- Optimized version using soft pointers for assets. 

- EnqueueFromDataTableRow : UFUNCTION(BlueprintCallable, 

- Category="Story") . Integrates with the Unreal Engine DataTable system for data-driven storytelling. 

- All functions utilize meta=(WorldContext="WorldContextObject") to automatically resolve the calling context. 

#### 4. **Component Architecture** : 

Inherits from UBlueprintFunctionLibrary . It is a stateless utility class and does not utilize a constructor for component initialization or scene attachment. 

#### 5. **Network/Replication** : 

Functions are executed locally. Since it interacts with UGameInstanceSubsystem , the effects (UI widgets) are inherently client-side. There is no internal RPC or property replication logic; network synchronization of story triggers must be handled at the Actor/GameState level before calling these functions. 

# **Camera Advanced Systems: Technical Documentation** 

This document covers the technical implementation of the Reinforcement Learning (RL), Memory, and Behavior Tree (BT) sub-modules used for automated camera and agent control. 

### **URTSRuleBasedDeciderComponent** 

1. **Purpose** : Provides a logic-driven decision engine that evaluates the current game state against designerdefined rules in DataTables to output camera/ability actions. 

2. **Logic & Algorithms (CPP Analysis)** : 

   - **Weighted Random Selection** : In EvaluateRulesFromDataTable , multiple matching rules are aggregated. A weighted random selection is performed based on the Frequency property of each FRTSRuleRow . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

21/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Attack-Return Sequence** : ExecuteAttackRuleRow captures the agent's current location, moves it to a target (ground-adjusted via LineTraceSingleByChannel and 

      - ProjectPointToNavigation ), executes actions, and schedules a return via 

      - AttackReturnDelaySeconds using a FTimerHandle and a weak pointer lambda. 

   - **Ground Alignment** : Uses a vertical trace from +10000.f to -10000.f relative to the agent's current Z to find ground height, then adds capsule half-height clearance to prevent sinking. 

3. **Blueprint & AI Interface** : 

   - **DataTables** : RulesDataTable (general strategy) and AttackRulesDataTable (combat strategy). 

   - **Wander Settings** : bEnableWander , bBiasTowardEnemy , WanderMinSameDirectionRepeats . 

   - **Function** : ChooseJsonActionRuleBased is the primary entry point for AI tasks. 

4. **Integration** : Attached as a component to ARLAgent . It provides raw JSON strings that are fed into UInferenceComponent::ExecuteActionFromJSON . 

5. **Network/Replication** : The component logic is primarily executed on the authority (AI Controller side), while the resulting actions are dispatched via the agent's replicated action system. 

### **ARTSBTController** 

1. **Purpose** : A specialized AI Controller designed to orchestrate camera AI using Behavior Trees, supporting both direct possession and "orchestrator" modes. 

2. **Logic & Algorithms (CPP Analysis)** : 

   - **Service Watchdog** : Implements a safety mechanism where NotifyBBServiceTick updates LastBBServiceTickTime . If Tick detects a timeout 

      - ( BBServiceWatchdogTimeout ), it automatically enables 

      - bEnableControllerBBUpdates to prevent the BT from stalling if a Service stops ticking. 

   - **Action Consumption** : ConsumeSelectedActionJSON implements a "read-and-clear" pattern on the Blackboard. It fetches the string from SelectedActionJSONKey and sets it to empty, ensuring the BT must produce a new decision for the next frame. 

   - **Team Resolution** : Iterates through all ARLAgent actors in the world to find one matching its OrchestratorTeamId to gather FGameStateData . 

3. **Blueprint & AI Interface** : 

   - **AI Assets** : StrategyBehaviorTree , SelectedActionJSONKey . 

   - **Update Logic** : bUseTickForBBUpdates , BlackboardUpdateInterval . 

4. **Integration** : Manages the lifecycle of the UBehaviorTreeComponent . It acts as the bridge between the Blackboard's output ( SelectedActionJSON ) and the ARLAgent 's execution engine. 

5. **Network/Replication** : Follows standard Unreal AI Controller replication. It typically runs on the Server. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

22/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **UInferenceComponent** 

1. **Purpose** : The central "Brain" component that toggles between ONNX-based Reinforcement Learning inference and Behavior Tree logic. 

2. **Logic & Algorithms (CPP Analysis)** : 

   - **NNE Integration** : Uses UE::NNE::INNERuntimeCPU to create a RuntimeModel from ONNX data. It performs synchronous inference via ModelInstance->RunSync . 

   - **Tensor Binding** : Maps a flat TArray<float> (21 features) to the input tensor. The output is an "Argmax" over the ActionSpace (36 possible actions). 

   - **Action Serialization** : GetActionAsJSON maps internal indices to structured JSON objects containing type , input_value , alt , ctrl , action , and camera_state . 

   - **Multi-Action Support** : ExecuteActionFromJSON detects if the input string is a JSON Array ( [ ) or Object ( { ) and iterates through entries to execute sequences of actions in a single frame. 

3. **Blueprint & AI Interface** : 

   - **Configuration** : BrainMode (RL vs BT), QNetworkModelData (ONNX asset). 

   - **Events** : PerformParsedAction must be implemented in Blueprint to translate the parsed JSON into actual movement/input calls. 

4. **Integration** : Attached to ARLAgent . It is the "Consumer" of decisions made by ARTSBTController or the RL model. 

5. **Network/Replication** : Inference is local (usually Server-side for AI). The resulting PerformParsedAction calls are then replicated to clients if they involve visual state changes. 

### **UBTService_PushGameStateToBB** 

1. **Purpose** : A Behavior Tree Service that synchronizes the complex world game state into Blackboard keys for decision-making tasks. 

2. **Logic & Algorithms (CPP Analysis)** : 

   - **Robust Team Resolution** : It attempts to resolve the TeamId by checking the Owner Controller, then a CVar ( r.RTSBT.ForcedTeamId ), then the Blackboard, and finally a world-wide fallback. 

   - **Data Aggregation** : Calls ARLAgent::GatherGameState which iterates through all units and structures to calculate health sums, resource levels, and average group positions. 

   - **Efficiency** : Uses BlackboardComp->GetKeyID to validate keys once, though the implementation currently uses SafeSetBB helpers to avoid crashes if keys are missing from the BB asset. 

3. **Blueprint & AI Interface** : 

   - **Key Mapping** : Large list of FName properties ( PrimaryResourceKey , MyUnitCountKey , etc.) that must match the Blackboard asset. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

23/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Interval** : Inherits standard BT Service Interval for polling frequency. 

4. **Integration** : Sits at the root of a Behavior Tree. It effectively "pumps" data from the 

   - ResourceGameState and ARLAgent into the BT's memory. 

5. **Network/Replication** : Runs on the authority owning the Behavior Tree. 

### **UBTT_ChooseAction_RuleBased** 

1. **Purpose** : A Behavior Tree Task that bridges the BT to the URTSRuleBasedDeciderComponent for high-level tactical decisions. 

2. **Logic & Algorithms (CPP Analysis)** : 

   - **State Reconstruction** : Reads dozens of keys from the Blackboard (Float, Int, Vector) to reconstruct an FGameStateData struct. 

   - **Hybrid Execution** : Supports bExecuteActionImmediately . If true, it bypasses the Controller's dispatch logic and calls Inference->ExecuteActionFromJSON directly from the task. 

   - **Pawn Resolution** : Attempts to find the APawn through the AAIController , the BTComponent owner, or an AgentPawnKey in the Blackboard. 

3. **Blueprint & AI Interface** : 

   - **Execution Controls** : bExecuteActionImmediately , bAlsoWriteToBB . 

   - **Debug** : bDebug enables verbose logging of the FGameStateData snapshot used for the decision. 

4. **Integration** : Leaf node in a Behavior Tree. Depends on URTSRuleBasedDeciderComponent being present on the agent pawn. 

5. **Network/Replication** : Logic is Server-side; execution results in Server-side input changes that replicate via the standard Pawn/Actor systems. 

# **Camera System: Technical Deep Dive** 

This document provides a technical overview of the camera classes within the RTS Unit Template, detailing their movement logic, input handling, and architectural design. 

### **ACameraBase** 

1. **Purpose** : The foundational camera pawn responsible for core movement (WASD, edge scrolling), smooth zooming, boundary clamping, and terrain-following logic. 

2. **Implementation (CPP Analysis)** : 

   - **Movement** : MoveInDirection calculates a world-space direction vector by rotating the input direction with the SpringArmRotator.Yaw . It uses FMath::Cos and FMath::Sin to transform local coordinates into world coordinates. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

24/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Terrain Following** : Within MoveInDirection , it performs a LineTraceSingleByChannel vertically to detect ALandscape actors, adjusting the pawn's Z-height to maintain a minimum clearance. 

   - **Boundary Clamping** : Movement is restricted by CameraPositionMin and CameraPositionMax . If UseNavBoundMinMax is true, these are automatically initialized in BeginPlay by iterating through ANavMeshBoundsVolume actors using TActorIterator . 

   - **Smooth Zooming** : ZoomIn and ZoomOut manipulate CurrentCamSpeed.Z using ZoomAccelerationRate and ZoomDecelerationRate . This speed is then applied to the SpringArm->TargetArmLength every update to provide a non-linear, weighted zoom feel. 

3. **Blueprint Interface** : 

   - **Movement Parameters** : CamSpeed , EdgeScrollCamSpeed , AccelerationRate , DecelerationRate . 

   - **Zoom Constraints** : ZoomSpeed , SpringArmMinRotator (Max Tilt), SpringArmMaxRotator (Min Tilt). 

   - **Limits** : CameraPositionMin/Max (FVector2D), UseNavBoundMinMax (bool). 

4. **Component Architecture** : 

   - **USpringArmComponent** : The "boom" for the camera. Initialized with bDoCollisionTest = false to prevent the camera from snapping when passing over units. 

   - **UCameraComponent** : Attached to the Spring Arm, providing the actual viewport. 

5. **Network/Replication** : 

   - BlockControls is replicated to allow servers to freeze player input during cutscenes or loading. 

   - SpringArm is explicitly set to replicate ( SetIsReplicated(true) ) to ensure consistent 

   - boom lengths across clients. 

### **AExtendedCameraBase** 

1. **Purpose** : Extends the base camera with high-level RTS features, including complex UI widget management (Abilities, Talents, Resources) and a state-driven input system. 

2. **Implementation (CPP Analysis)** : 

   - **Input State Machine** : SwitchControllerStateMachine acts as a central dispatcher for Enhanced Input. It uses bit-flags or state IDs to trigger complex behaviors like unit selection by tag, ability execution, or camera rotations, accounting for IsCtrlPressed and AltIsPressed modifiers. 

   - **UI Flow** : Input_Tab_Pressed cycles through TabMode (Resources -> Controls -> Win Conditions). It calls UpdateTabModeUI which toggles ESlateVisibility for various widgets. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

25/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Viewport Effects** : UpdateViewportBlur dynamically modifies PostProcessSettings on the CameraComp . It overrides DepthOfFieldFocalDistance and DepthOfFieldFstop to create a heavy blur when the UI menu is open. 

   - **Ability Integration** : ExecuteOnAbilityInputDetected bridges the camera input to the ACameraControllerBase , triggering mass ability activations on selected units. 

3. **Blueprint Interface** : 

   - **Widgets** : Minimap , ResourceWidget , TalentChooserWidget , AbilityChooserWidget , MapMenuWidget . 

   - **Configuration** : TagTime (Time held to assign a control group), AutoAdjustTalentChooserPosition . 

4. **Component Architecture** : Inherits from ACameraBase . It primarily manages the lifecycle and eventbinding of several UUserWidget subclasses. 

5. **Network/Replication** : 

   - Client_UpdateWidgets : A Reliable Client RPC used to initialize widget references on the client 

   - side from the server's authoritative state. 

   - Replicates team-based data to update the WinConditionWidget correctly. 

### **AAdvancedCameraBase** 

1. **Purpose** : A specialized camera used for maps or scenarios where a physical platform (e.g., a "Command Deck") needs to follow the camera view. 

2. **Implementation (CPP Analysis)** : 

   - **Platform Attachment** : CustomSpawnPlatform calculates a world-space location using the camera's GetForwardVector , GetRightVector , and GetUpVector multiplied by CustomPlatformOffset . 

   - **Lifecycle** : Spawns an AUnitSpawnPlatform using SpawnActor and immediately calls AttachToComponent(CameraComp, 

   - FAttachmentTransformRules::KeepWorldTransform) . This ensures the platform perfectly tracks camera translation and rotation. 

3. **Blueprint Interface** : 

   - **Platform Settings** : CustomSpawnPlatformClass (TSubclassOf), CustomPlatformOffset (FVector). 

   - **Reference** : CustomAttachedPlatform (BlueprintReadOnly). 

4. **Component Architecture** : Inherits from AExtendedCameraBase . It does not add new internal components but manages an external Actor attachment. 

5. **Network/Replication** : Inherits replication from parents; the platform itself manages its own replication. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

26/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **ARLAgent** 

1. **Purpose** : A Reinforcement Learning (RL) specialized camera agent. It serves as the interface between the Unreal simulation and an external training process or internal AI model. 

2. **Implementation (CPP Analysis)** : 

   - **Data Serialization** : CreateGameStateJSON uses FString::Printf to manually construct a JSON representation of the FGameStateData . This includes unit counts, health sums, average positions, and resource levels. 

   - **Inter-Process Communication** : AgentInitialization creates an FSharedMemoryManager mapped to a TeamID-specific memory segment. This is used for low- 

   - latency data exchange with external Python/C++ RL trainers. 

   - **Action Execution** : ReceiveRLAction parses incoming JSON actions using TJsonReader . It maps action strings (e.g., "move_camera", "left_click") to existing pawn and controller functions. 

   - **Game State Gathering** : GatherGameState iterates through GameMode->AllUnits , aggregating AttributeSet data and calculating the AverageFriendlyPosition and AverageEnemyPosition . 

3. **Blueprint Interface** : 

   - **Training Config** : bIsTraining (Toggles state requests), bEnableSharedMemoryIO (Toggles external IPC). 

   - **Movement Scale** : DeltaMovement (Fixed distance per discrete RL action). 

   - **Debug** : bDebug (Enables verbose logging of agent decisions). 

4. **Component Architecture** : 

   - **UInferenceComponent** : An internal component used to load and run models (like ONNX or internal logic) to choose actions when not using shared memory. 

5. **Network/Replication** : 

   - Server_RequestGameState / Client_ReceiveGameState : Reliable RPCs used to 

   - fetch authority-side game data and deliver it to the client-side RL agent. 

# **Camera Technical Documentation** 

This document provides a technical deep-dive into the RTS Camera system, covering the hierarchy from base functionality to RL-integrated agents. 

### **ACameraBase** 

1. **Purpose** : Acts as the foundation for the RTS camera system, providing core movement (panning), zooming, rotation, and coordinate-space boundary clamping. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

27/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Movement** : MoveInDirection calculates world direction by rotating input vectors against the SpringArm yaw using Sine/Cosine. It includes a line trace to adjust Z-height against ALandscape and clamps the final position within CameraPositionMin/Max . 

   - **Zooming** : ZoomIn and ZoomOut use acceleration/deceleration logic to modify SpringArm>TargetArmLength . 

   - **Rotation** : RotateCamera and OrbitCamLeft handle Yaw adjustments. RotateCamera uses a RotationIncreaser for smooth transitions and normalizes Yaw to a [0, 360) range. 

   - **Boundaries** : In BeginPlay , if UseNavBoundMinMax is true, it iterates through ANavMeshBoundsVolume actors to automatically calculate camera movement limits. 

3. **Blueprint Interface** : 

   - **Properties** : CamSpeed , ZoomSpeed , AccelerationRate , CameraPositionMin/Max , UseNavBoundMinMax , CameraState (TEnumAsByte). 

   - **Functions** : SetCameraState , JumpCamera (teleport to hit location), LockOnUnit . 

#### 4. **Component Architecture** : 

- USpringArmComponent : Handles the distance and rotation of the camera relative to the pawn 

- root. 

- UCameraComponent : Attached to the SpringArm for the actual view rendering. 

- UCapsuleComponent : Inherited from ACharacter, used for basic collision and as an attachment 

- parent. 

#### 5. **Network/Replication** : 

- BlockControls : Replicated boolean to disable input. 

- SpringArm : Set to replicate to ensure camera distance/rotation consistency across clients if 

- needed. 

- Uses GetLifetimeReplicatedProps for state synchronization. 

### **AExtendedCameraBase** 

1. **Purpose** : Extends the base camera with UI management, specialized input handling via Enhanced Input, and a state-machine approach to controller interaction. 

2. **Implementation (CPP Analysis)** : 

   - **State Management** : SwitchControllerStateMachine is a massive dispatcher that translates input IDs into specific logic (e.g., camera moves, ability triggers, selection) based on modifier keys (Ctrl/Alt). 

   - **UI Logic** : UpdateTabModeUI cycles through TabMode (Resources, Controls, Win Conditions) and manages widget visibility and CameraComp post-process blur settings for a "focus" effect. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

28/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Win Conditions** : Binds to AWinLoseConfigActor delegates ( OnWinConditionChanged , OnTagProgressUpdated ) to dynamically show/hide the WinConditionWidget . 

3. **Blueprint Interface** : 

   - **Properties** : References to various UUserWidgets ( ResourceWidget , TalentChooserWidget , MapMenuWidget , etc.), TagTime (hold duration for F-key 

   - tagging). 

   - **Functions** : UpdateTabModeUI , ExecuteOnAbilityInputDetected , InitializeWinConditionDisplay . 

#### 4. **Component Architecture** : 

   - Adds LoadingWidgetComp (UWidgetComponent) for in-world 3D UI display. 

   - Inherits SpringArm and CameraComp from ACameraBase . 

5. **Network/Replication** : 

   - Client_UpdateWidgets : A Client-only Reliable RPC to synchronize widget references from the 

   - server to the local client. 

   - Disables movement replication in constructor ( SetReplicatingMovement(false) ) as RTS cameras are typically locally controlled with server-side validation of actions rather than position. 

### **AAdvancedCameraBase** 

1. **Purpose** : Provides specialized functionality for spawning and attaching a unit spawn platform that follows the camera's movement and rotation. 

2. **Implementation (CPP Analysis)** : 

   - **Spawn Logic** : CustomSpawnPlatform uses FActorSpawnParameters with AlwaysSpawn . It calculates a world-space location using the camera's local axes: ForwardVector * X + RightVector * Y + UpVector * Z . 

   - **Attachment** : Once spawned, the platform is attached to CameraComp using FAttachmentTransformRules::KeepWorldTransform . 

   - **Initialization** : Calls the spawn logic immediately in BeginPlay . 

3. **Blueprint Interface** : 

   - **Properties** : CustomPlatformOffset (FVector), CustomSpawnPlatformClass (TSubclassOf), CustomAttachedPlatform (Reference). 

   - **Functions** : CustomSpawnPlatform (BlueprintCallable). 

4. **Component Architecture** : Inherits from AExtendedCameraBase . No additional internal components beyond the external actor attachment. 

5. **Network/Replication** : Inherits base replication. The spawned platform actor typically handles its own replication if configured in its class. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

29/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **ARLAgent** 

1. **Purpose** : A specialized camera pawn designed for Reinforcement Learning, capable of gathering game state and executing actions via Shared Memory or an Inference Component. 

2. **Implementation (CPP Analysis)** : 

   - **Data Gathering** : GatherGameState iterates through all units in AUpgradeGameMode , aggregating counts, health, damage, and positions for both friendly and enemy teams, including per-tag unit counts. 

   - **RL Loop** : UpdateGameState (timer-driven) triggers server RPCs. Client_ReceiveGameState writes JSON data to shared memory via FSharedMemoryManager . CheckForNewActions reads actions back from memory. 

   - **Action Execution** : ReceiveRLAction parses JSON strings into commands like move_camera , left_click , right_click , and resource_management . It implements custom 

   - boundary logic using actors tagged RLAgentCameraBounds . 

3. **Blueprint Interface** : 

   - **Properties** : bIsTraining , bEnableSharedMemoryIO , DeltaMovement , FallbackBounceDelta . 

   - **Functions** : ReceiveRLAction , AgentInitialization . 

4. **Component Architecture** : 

   - UInferenceComponent : Subobject used for local decision making when Shared Memory IO is 

   - disabled. 

5. **Network/Replication** : 

   - Server_PlayGame / Server_RequestGameState : Server RPCs to aggregate state and 

   - process model decisions on the authority side. 

   - Client_ReceiveGameState : Client RPC to pipe server-side state to the RL process. 

# **Characters/Camera/BehaviorTree Technical Documentation** 

This document provides a technical deep-dive into the Behavior Tree module for the RTS Unit Template camera and agent systems. 

### **UBTService_PushGameStateToBB** 

1. **Purpose** : Periodically aggregates global game state from the perspective of a specific team and pushes it into the Blackboard to drive high-level AI decision-making. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

30/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Team Resolution** : In PushOnce , it resolves the active TeamId by checking the Owner Controller (checking for ARTSBTController or AExtendedControllerBase ), a ForcedTeamId property, a Blackboard value, or falling back to a world search for controllers. 

   - **Data Retrieval** : Uses UGameplayStatics::GetAllActorsOfClass to find an ARLAgent and calls RLAgent->GatherGameState(TeamId) to populate an FGameStateData struct. 

   - **BB Injection** : Uses lambda helpers SafeSetBBFloat and SafeSetBBInt to validate Blackboard key existence via BB->GetKeyID before calling SetValueAsFloat/Int . 

   - **Tick Logic** : Configured with bCallTickOnSearchStart = true and bRestartTimerOnEachActivation = false to ensure data is available immediately upon 

   - branch entry. 

3. **Blueprint Interface** : 

   - UPROPERTY keys for unit counts, health, and 6 resource tiers (Primary through Legendary). 

   - UPROPERTY keys for AgentPosition , AverageFriendlyPosition , and AverageEnemyPosition . 

   - bDebug flag for logging resource and position snapshots. 

4. **Component Architecture** : Inherits from UBTService . Sets NodeName = TEXT("Push GameState To Blackboard") . Constructor sets Interval = 0.1f . 

5. **Network/Replication** : Executed locally on the server (or client-side AI owner). Relies on ARLAgent gathering data from local or replicated game state. 

### **UBTService_UpdateAgentPosition** 

1. **Purpose** : A lightweight service to keep a Vector blackboard key synchronized with the controlled pawn's world location. 

2. **Implementation (CPP Analysis)** : 

   - **Location Logic** : Inside TickNode , it retrieves the AAIController owner, gets the possessed APawn , and calls Pawn->GetActorLocation() . 

   - **BB Update** : Directly calls BB->SetValueAsVector using the AgentPositionKey . 

3. **Blueprint Interface** : 

   - UPROPERTY AgentPositionKey (default: "AgentPosition"). 

   - Interval (default: 0.2f). 

4. **Component Architecture** : Inherits from UBTService . Disables bNotifyBecomeRelevant and bNotifyCeaseRelevant to minimize overhead. 

5. **Network/Replication** : Runs on the AI authority. 

### **ARTSBTController** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

31/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : The primary AI Controller that runs the Behavior Tree and acts as the interface between the AI logic (Blackboard) and the Pawn's execution (InferenceComponent). 

2. **Implementation (CPP Analysis)** : 

   - **Execution** : RunBehaviorTree is called in BeginPlay (for orchestrators) and OnPossess . 

   - **Watchdog Mechanism** : Monitors the last time a BT Service pinged via NotifyBBServiceTick . If LastBBServiceTickTime exceeds BBServiceWatchdogTimeout , it engages bControllerBBFallbackEngaged and starts its own BB update loop. 

   - **Action Consumption** : In Tick , it calls ConsumeSelectedActionJSON , which reads SelectedActionJSONKey from BB. If non-empty and unique, it clears the BB value and 

   - dispatches it to the ARLAgent via Inf->ExecuteActionFromJSON . 

   - **BB Push** : PushBlackboardFromGameState_ControllerOwned provides a fallback mechanism to populate the BB if services are not active, using RLAgent->GatherGameState . 

3. **Blueprint Interface** : 

   - StrategyBehaviorTree : The UBehaviorTree asset to execute. 

   - OrchestratorTeamId : Explicit team ID for scenarios without pawn possession. 

   - bEnableControllerBBUpdates : Toggle for the internal BB update loop. 

4. **Component Architecture** : Inherits from AAIController . Manages BBUpdateTimerHandle for timer-based updates and BBUpdateAccumulator for tick-based cadence. 

5. **Network/Replication** : Standard AI Controller replication. Action dispatch happens on the server. 

### **UBTT_ChooseActionByIndex** 

1. **Purpose** : A Behavior Tree task that writes a specific, pre-defined action index to the Blackboard as a JSON string. 

2. **Implementation (CPP Analysis)** : 

   - **JSON Translation** : Resolves the Pawn's UInferenceComponent and calls GetActionAsJSON with the Action enum value cast to int32 . 

   - **BB Write** : Uses SetValueAsString on the key specified by GetSelectedBlackboardKey() . 

3. **Blueprint Interface** : 

   - Action : Enum of type ERTSAIAction to select the specific action. 

   - bDebug : Toggle for error logging if the InferenceComponent is missing. 

4. **Component Architecture** : Inherits from UBTT_BlackboardBase . Constructor adds a string filter to the BlackboardKey . 

5. **Network/Replication** : Executes on the server within the BT execution flow. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

32/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **UBTT_ChooseAction_RuleBased** 

1. **Purpose** : Bridges the Blackboard state with the URTSRuleBasedDeciderComponent to select actions based on complex heuristics and DataTables. 

2. **Implementation (CPP Analysis)** : 

   - **State Reconstruction** : Reads a wide array of BB keys (UnitCounts, Resources, Positions) into an FGameStateData struct. 

   - **Pawn Resolution** : Robustly finds the APawn by checking the AI Owner, the AgentPawnKey in BB, or the BT Component owner. 

   - **Immediate Execution** : If bExecuteActionImmediately is true, it calls Inference>ExecuteActionFromJSON directly within the task, bypassing the Controller's tick consumption. 

3. **Blueprint Interface** : 

   - Comprehensive set of FName keys for all FGameStateData fields. 

   - bExecuteActionImmediately : Whether to execute on the pawn immediately. 

   - bAlsoWriteToBB : Whether to still write the JSON to Blackboard when executing immediately. 

4. **Component Architecture** : Inherits from UBTT_BlackboardBase . Uses GET_MEMBER_NAME_CHECKED for string filtering. 

5. **Network/Replication** : Runs on AI authority. 

### **UBTT_ExampleDecideAction** 

1. **Purpose** : A reference implementation for simple branching logic within a C++ task node. 

2. **Implementation (CPP Analysis)** : 

   - **Logic** : Compares MyUnitCountKey and EnemyUnitCountKey from BB. 

   - **Branching** : Calculates Diff = MyCount - EnemyCount and checks against AdvantageThreshold to pick between ActionIfAdvantage or ActionIfDisadvantage . 

   - **Translation** : Uses InferenceComp->GetActionAsJSON to convert the chosen enum to a JSON string. 

3. **Blueprint Interface** : 

   - AdvantageThreshold : Int threshold for comparison. 

   - ActionIfAdvantage / ActionIfDisadvantage : Enums of type ERTSAIAction . 

4. **Component Architecture** : Inherits from UBTT_BlackboardBase . 

5. **Network/Replication** : Runs on AI authority. 

### **URTSRuleBasedDeciderComponent** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

33/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : The core logic engine for rule-based AI. It evaluates game state against DataTables and handles spatial fallbacks like camera wandering and attack sequences. 

2. **Implementation (CPP Analysis)** : 

   - **Rule Evaluation** : EvaluateRuleRow checks GameTimeCap , resource costs (handling Supplytype resources differently via AResourceGameState ), and UnitCaps (supporting AND/OR logic). 

   - **Attack Sequences** : ExecuteAttackRuleRow teleports the ARLAgent to a target position. It calculates ground adjustment using LineTraceSingleByChannel and validates the point using UNavigationSystemV1::ProjectPointToNavigation . 

   - **Attack Block & Return** : Uses bAttackReturnBlockActive to prevent new decisions during an attack. FinalizeAttackReturn handles the teleport back and executes a left_click 1 post-action. 

   - **Wander Logic** : PickWanderActionIndex selects camera movement directions. It enforces WanderMinSameDirectionRepeats to prevent erratic camera jitter. 

   - **Spatial Search** : PopulateAttackPositions uses TActorIterator to find enemy units/buildings of specific classes and caches their locations. 

3. **Blueprint Interface** : 

   - bUseDataTableRules / RulesDataTable : Normal logic (e.g. build orders). 

   - bUseAttackDataTableRules / AttackRulesDataTable : High-priority spatial logic. 

   - AttackRuleCheckIntervalSeconds : Cooldown between attack evaluations. 

   - WanderTwoStep : Toggle for Selection -> Move wander behavior. 

4. **Component Architecture** : UActorComponent . Uses FTimerHandle for position refreshing and attack returns. 

5. **Network/Replication** : Intended to run on the server. NavMesh projection relies on server-side navigation data. 

# **Characters/Camera/Memory Technical Documentation** 

### **SharedData** 

1. **Purpose** : Defines the fixed-size binary layout for the shared memory region used for Inter-Process Communication (IPC). 

2. **Implementation (CPP Analysis)** : 

   - A Plain Old Data (POD) structure designed for memory mapping. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

34/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - Uses TCHAR arrays of size 1024 for GameState and Action to support Unreal's string format (UTF-16 on Windows). 

   - Contains bool flags ( bNewGameStateAvailable , bNewActionAvailable ) used as primitive synchronization primitives between processes. 

3. **Blueprint Interface** : N/A. This is a raw C++ struct. 

4. **Component Architecture** : Data structure mapped directly to a file-backed memory region. 

5. **Network/Replication** : None. Local system IPC only. 

### **FSharedMemoryManager** 

1. **Purpose** : Manages the lifecycle of Windows named shared memory and provides an API for writing game state and reading actions. 

2. **Implementation (CPP Analysis)** : 

   - **Constructor** : Prepends Global\ to the mapping name for session-wide visibility. Invokes CreateFileMapping with INVALID_HANDLE_VALUE (paging file) and MapViewOfFile to get a pointer to the SharedData struct. 

   - **Destructor** : Performs resource cleanup using UnmapViewOfFile and CloseHandle to release OS handles. 

   - 

      - **WriteGameState** : 

      - Takes an FString JSON representation. 

      - Calculates copy size using FMath::Min(StringLength, BufferSizeInChars - 1) * sizeof(TCHAR) . 

      - Uses FMemory::Memcpy to move data into the mapped region. 

      - Manually null-terminates the buffer at SharedDataPtr->GameState[BytesToCopy / sizeof(TCHAR)] . 

      - Sets bNewGameStateAvailable = true . 

   - **ReadAction** : 

      - Polls bNewActionAvailable . 

      - If true, converts the TCHAR buffer SharedDataPtr->Action into an FString . 

      - Resets the bNewActionAvailable flag to false. 

3. **Blueprint Interface** : None. This is a pure C++ manager class. 

4. **Component Architecture** : Standalone C++ class. It encapsulates raw Windows API handles ( HANDLE ) and a pointer to the shared memory region ( SharedDataPtr ). 

5. **Network/Replication** : None. This mechanism operates outside of the Unreal Engine networking stack, specifically for communication with external local processes. 

### **FRLAction** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

35/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Encapsulates a discrete control command within the Reinforcement Learning action space, optimized for JSON serialization and transfer to the agent's control logic. 

2. **Implementation (CPP Analysis)** : 

   - Provides a specialized constructor for stack-allocation during the initialization of the action space. 

   - The struct is designed to map directly to the ARLAgent 's input processing, utilizing primitive types that mirror JSON fields. 

3. **Blueprint Interface** : 

   - UPROPERTY fields: Type (Control type), InputValue (Analog weight), bAlt / bCtrl (Mod 

   - keys), Action (Action identifier), CameraState (Target index). 

4. **Component Architecture** : Defined as a USTRUCT(BlueprintType) used as the element type for the ActionSpace array in UInferenceComponent . 

5. **Network/Replication** : No internal replication; state is handled via local execution or higher-level JSON serialization. 

### **FGameStateData** 

1. **Purpose** : Provides a standardized snapshot of the world state, encompassing unit metrics, resources, and spatial data for inference. 

2. **Implementation (CPP Analysis)** : 

   - Acts as a data-heavy container used to feed the 21-feature vector for the ONNX model and 40+ keys for the Blackboard. 

   - Includes unit counts per tag (Alt1-6, Ctrl1-6, CtrlQ/W/E/R) to support strategic decision-making in the Behavior Tree. 

3. **Blueprint Interface** : 

   - Fully exposed via BlueprintReadWrite across multiple categories: Unit counts, health/damage metrics, FVector spatial data, resource counts, and resource caps. 

4. **Component Architecture** : USTRUCT(BlueprintType) used as the primary input interface for all decision-making methods. 

5. **Network/Replication** : Pure data structure; replication is handled at the Actor level before the struct is populated. 

### **UInferenceComponent** 

1. **Purpose** : Orchestrates AI decision-making by routing game state data through either a Reinforcement Learning model (via NNE) or a traditional Behavior Tree. 

2. **Implementation (CPP Analysis)** : 

   - **NNE Lifecycle** : BeginPlay retrieves the NNERuntimeORTCpu CPU runtime. It initializes a TSharedPtr<IModelCPU> and creates a IModelInstanceCPU . SetInputTensorShapes is used to define a 1x21 input tensor. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

36/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

- **State Flattening** : ConvertStateToArray performs manual serialization of FGameStateData into a TArray<float> , maintaining strict ordinal alignment with the trained 

- model's input layer. 

- **Sync Inference** : GetActionFromRLModel utilizes FTensorBindingCPU to bind raw pointer data from the converted array and the output Q-value buffer. It executes RunSync and implements an Argmax algorithm to derive the optimal ActionIndex . 

- **BT Execution** : ChooseJsonAction implements brain routing. For BT mode, it manually triggers BehaviorTreeComp->TickComponent after refreshing the Blackboard via UpdateBlackboard . It retrieves the result from the SelectedActionJSON Blackboard key. 

- **JSON Dispatch** : ExecuteActionFromJSON parses input via TJsonReader and FJsonSerializer . It handles both single objects and TArray<TSharedPtr<FJsonValue>> (bulk actions), forwarding them to the ARLAgent::ReceiveRLAction . 

#### 3. **Blueprint Interface** : 

- UPROPERTIES : BrainMode (EBrainMode), StrategyBehaviorTree (UBehaviorTree*), QNetworkModelData (UNNEModelData*). 

- UFUNCTIONS : ChooseAction , ChooseJsonAction , ExecuteActionFromJSON , PushBlackboardFromGameState , GetActionAsJSON . 

- Events : PerformParsedAction provides a hook for Blueprint-side logic execution. 

#### 4. **Component Architecture** : 

   - Disables ticking ( bCanEverTick = false ) as inference is event-driven (timer or request-based). 

   - InitializeActionSpace populates the 36-index action map corresponding to the model's 

   - output neurons. 

5. **Network/Replication** : Local component execution; not marked for replication. Assumes execution on the authority or autonomous proxy. 

# **Characters/Camera Technical Documentation** 

### **ACameraBase** 

1. **Purpose** : Core base class for the RTS camera system, providing basic movement, zooming, rotation, and terrain-following capabilities for the player's viewpoint. 

2. **Implementation (CPP Analysis)** : 

   - **Movement** : MoveInDirection uses trigonometric functions ( FMath::Cos / FMath::Sin ) based on SpringArmRotator.Yaw to calculate world-space direction from local input. It includes terrain following via LineTraceSingleByChannel against ECC_WorldStatic to adjust Z-height and clamps position within CameraPositionMin/Max . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

37/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Zooming** : ZoomIn and ZoomOut implement a velocity-based system using ZoomAccelerationRate and ZoomDecelerationRate to modify SpringArm- 

   - >TargetArmLength . 

   - **Rotation** : RotateCamera and OrbitCamLeft handle Yaw manipulation with interpolation and normalization to [0, 360). IsCameraInAngle checks alignment with predefined 

      - CameraAngles . 

   - **Spatial Constraints** : BeginPlay automatically populates camera bounds from the first ANavMeshBoundsVolume found in the level if UseNavBoundMinMax is true. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : Configurable speeds ( CamSpeed , ZoomSpeed ), rotation limits ( SpringArmMin/MaxRotator ), and camera angles. Exposed component pointers for SpringArm and CameraComp . 

   - **UFUNCTIONS** : SetCameraState , JumpCamera , LockOnUnit , and various Zoom/Rotate utilities are BlueprintCallable . 

4. **Component Architecture** : 

   - Constructor initializes a UCapsuleComponent (via ACharacter ) as the physics root. 

   - CreateCameraComp (called during initialization) sets up USpringArmComponent attached 

   - to the capsule, and UCameraComponent attached to the spring arm. 

5. **Network/Replication** : 

   - BlockControls is replicated via DOREPLIFETIME . 

   - SpringArm is explicitly set to replicate ( SetIsReplicated(true) ). 

### **AExtendedCameraBase** 

1. **Purpose** : Extension of the base camera to handle complex UI management, RTS-specific input processing, and game state integration (Win/Lose conditions). 

2. **Implementation (CPP Analysis)** : 

- **Input Mapping** : SetupPlayerInputComponent utilizes UEnhancedInputComponentBase to bind FGameplayTag identifiers to member functions. 

- **State Machine** : SwitchControllerStateMachine acts as a central dispatcher, routing raw input actions to specific logic (abilities, selection, camera modes) based on modifier keys ( IsCtrlPressed , AltIsPressed ). 

- **UI Logic** : UpdateTabModeUI manages visibility of ResourceWidget , WinConditionWidget , and MapMenuWidget . It applies post-process blur to the CameraComp when the menu is active by overriding Depth of Field settings. 

- **Event Handling** : InitializeWinConditionDisplay binds to AWinLoseConfigActor delegates ( OnWinConditionChanged , OnTagProgressUpdated ) to trigger UI feedback. 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

38/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **UPROPERTIES** : Pointers to various UMG widgets ( TalentChooserWidget , UnitSelectorWidget , etc.) and the InputConfig data asset. 

   - **UFUNCTIONS** : Implementation of specialized input handlers ( Input_LeftClick_Pressed , Input_Tab_Pressed ) and UI update triggers. 

4. **Component Architecture** : Inherits the ACameraBase hierarchy. Configures the capsule and mesh collision responses to ignore pawns while blocking world static geometry in the constructor. 

5. **Network/Replication** : 

   - Client_UpdateWidgets is a Reliable Client RPC used to synchronize widget pointers 

   - from the server to the local client. 

   - Leverages base class BlockControls replication. 

### **AAdvancedCameraBase** 

1. **Purpose** : A specialized camera variant that supports an attached physical platform for spawning units or other gameplay actors. 

2. **Implementation (CPP Analysis)** : 

   - **Spawn Logic** : CustomSpawnPlatform uses GetWorld()->SpawnActor to instantiate an AUnitSpawnPlatform using a TSubclassOf reference. 

   - **Attachment** : The spawned platform is attached to CameraComp using KeepWorldTransform . Its location is calculated dynamically relative to the camera's forward, right, and up vectors using CustomPlatformOffset . 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : CustomPlatformOffset (FVector), CustomSpawnPlatformClass (TSubclassOf), and a reference to the spawned CustomAttachedPlatform . 

   - **UFUNCTIONS** : CustomSpawnPlatform is BlueprintCallable to allow manual retriggering of the platform setup. 

4. **Component Architecture** : Inherits from AExtendedCameraBase . It does not add new components in the constructor but manages the lifecycle of an external actor. 

5. **Network/Replication** : Relies on the standard Actor attachment replication and base class replication features. 

### **ARLAgent** 

1. **Purpose** : A Reinforcement Learning (RL) enabled agent that provides an interface for external training scripts or internal AI behavior trees to control the camera and issue RTS commands. 

2. **Implementation (CPP Analysis)** : 

   - **Data Aggregation** : GatherGameState iterates through GameMode->AllUnits , calculating cumulative health, damage, and counts for friendly vs. enemy units, categorized by FGameplayTag (e.g., Ctrl1, Alt2). 

https://wiki.teufel-engineering.com/en/rts-unit-template 

39/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Action Processing** : ReceiveRLAction parses incoming JSON strings using FJsonSerializer . It maps JSON keys (action names, camera states) to native functions like SwitchControllerStateMachine , PerformLeftClickAction , or resource 

   - management calls. 

   - **IO Management** : UpdateGameState periodically triggers state gathering. If bEnableSharedMemoryIO is true, it uses FSharedMemoryManager for high-speed IPC 

   - with external processes. 

   - **Pathfinding Integration** : PerformRightClickAction and RunUnitsAndSetWaypoints interface with the controller to issue mass movement commands using grid-based offsets. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : InferenceComponent (UInferenceComponent), bIsTraining flag, and DeltaMovement for discrete RL step sizes. 

   - **UFUNCTIONS** : ReceiveRLAction for external control; Server_PlayGame for server-side inference. 

4. **Component Architecture** : Includes a UInferenceComponent in the constructor for Behavior Tree and model inference integration. 

5. **Network/Replication** : 

   - Server_RequestGameState : Server RPC to pull data from the authoritative GameMode. 

   - Client_ReceiveGameState : Client RPC to deliver processed data to the agent for RL 

   - consumption. 

   - Server_PlayGame : Server RPC that encapsulates the "Observe-Decide-Act" loop. 

# **Characters Unit Technical Documentation** 

### **ASpawnerUnit** 

1. **Purpose** : Primary base class for units, responsible for spawning mechanics, DataTable integration, and basic unit identification (Team/Squad). 

2. **Implementation (CPP Analysis)** : 

   - CreateSpawnDataFromDataTable() : Uses UDataTable::GetRowNames and FindRow<FSpawnData> to populate a local array for procedural spawning. 

   - SpawnPickupWithProbability() : Implements conditional spawning using FMath::RandRange(0.f, 100.f) against a probability threshold. 

   - UnitControlTimer : A replicated float used as a shared clock for state machine synchronization 

   - in AI controllers. 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

40/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Properties** : SpawnDataTable (UDataTable), UnitTags (FGameplayTagContainer), TeamId (int), SquadId (int). 

   - **Functions** : CreateSpawnDataFromDataTable , SpawnPickup , SpawnPickupsArray . 

4. **Component Architecture** : Extends ACharacter . Standard character components without additional sub-objects in the constructor. 

5. **Network/Replication** : Replicates TeamId , SquadId , UnitTags , and UnitControlTimer . Spawning logic is server-authoritative. 

### **AGASUnit** 

1. **Purpose** : Integration layer for the Unreal Gameplay Ability System (GAS), featuring a robust ability queuing mechanism. 

2. **Implementation (CPP Analysis)** : 

   - AbilityQueue : A TQueue<FQueuedAbility> that stores activation requests when the 

   - ASC is busy or on cooldown. 

   - ActivateAbilityByInputID() : Logic handles either immediate activation or enqueuing. It 

   - captures FHitResult and APlayerController for late activation. 

   - GetAbilityDisplayObject() : Manages a AbilityProxyCache (TMap) to provide UI- 

   - friendly proxy objects with synchronized ConstructionCost data on clients. 

3. **Blueprint Interface** : 

   - **Properties** : AbilitySystemComponent , Attributes . AbilityQueueSize , MaxAbilityQueueSize . DefaultAbilities through FourthAbilities . 

   - **Functions** : CancelCurrentAbility() , ActivateAbilityByInputID() , GetAbilityDisplayObject() . 

4. **Component Architecture** : 

   - UAbilitySystemComponentBase : Replicated using Minimal mode for performance. 

   - UAttributeSetBase : Holds replicated gameplay attributes. 

5. **Network/Replication** : Replicates ASC, Attributes, QueSnapshot , and ReplicatedAbilityCosts . UpdateReplicatedAbilityCost allows the server to 

broadcast dynamic price changes to client UIs. 

### **ALevelUnit** 

1. **Purpose** : Manages unit progression, experience scaling, and attribute/talent investment. 

2. **Implementation (CPP Analysis)** : 

   - Tick() : Implements server-side attribute regeneration for Health and Shield using Attributes- 

   - >SetAttribute... methods. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

41/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - LevelUp_Implementation() : Authoritative logic to increment level, award points, and 

   - consume XP. Triggers OnLevelUp BP event. 

   - ApplyInvestmentEffect() : Uses AbilitySystemComponent- 

   - >ApplyGameplayEffectToSelf to permanently modify attributes via talent investment. 

3. **Blueprint Interface** : 

   - **Properties** : LevelData , LevelUpData . Investment GE classes (e.g., StaminaInvestmentEffect ). AutolevelConfig . 

   - **Functions** : LevelUp() , AutoLevelUp() , InvestPointIntoStamina() , ResetTalents() . 

4. **Component Architecture** : Inherits from AGASUnit . 

5. **Network/Replication** : Replicates LevelData (using OnRep_LevelData for UI updates), LevelUpData , and all investment GameplayEffect classes. 

### **AAbilityUnit** 

1. **Purpose** : Orchestrates high-level unit states and specialized movement utilities (teleportation, acceleration). 

2. **Implementation (CPP Analysis)** : 

   - TeleportToValidLocation() : Uses LineTraceSingleByChannel for ground 

   - detection and valid placement. Crucially updates FMassAIStateFragment::StoredLocation to ensure Mass AI continuity. 

   - SetUnitState() : State machine transitioner that invokes BP implementable events (e.g., StartedMoving , GotAttacked ). 

   - Accelerate() : Timer-driven (0.1s) implementation using FMath::VInterpTo and LaunchCharacter for smooth physics-based movement. 

3. **Blueprint Interface** : 

   - **Properties** : UnitState , UnitStatePlaceholder . GAS Input IDs ( OffensiveAbilityID etc.). IsWorker . 

   - **Functions** : TeleportToValidLocation() , SetUnitState() , SpendAbilityPoints() . 

4. **Component Architecture** : Inherits from ALevelUnit . 

5. **Network/Replication** : Replicates UnitState , UnitStatePlaceholder , and StoredUnitState . 

### **AMassUnitBase** 

1. **Purpose** : Critical bridge between standard Actors and the high-performance Mass Entity Subsystem, providing visual synchronization for Mass entities. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

42/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - SyncTranslation() / SyncRotation() : Manual synchronization methods that push Actor 

   - state into Mass FTransformFragment . 

   - MulticastRotateActorLinear() / MulticastMoveISMLinear() : Smooth 

   - interpolation system that uses FTimerHandle (linear/easing) to move visuals on clients without full Actor ticks. 

   - StartCharge() : Injects FMassChargeTimerFragment and FMassStateChargingTag into the Mass entity to drive high-speed movement processors. 

3. **Blueprint Interface** : 

   - **Properties** : MassActorBindingComponent , ISMComponent . IsFlying , FlyHeight . 

   - **Functions** : StopMassMovement() , SetInvisibility() , SyncTranslation() , MulticastRotateISMLinear() . 

#### 4. **Component Architecture** : 

   - UMassActorBindingComponent : Primary Mass integration component. 

   - UInstancedStaticMeshComponent : Visual representation for Mass-driven units. 

   - USelectionDecalComponent : Selection visual. 

5. **Network/Replication** : Replicates visual state ( bUseSkeletalMovement , IsFlying ), ISM component reference, and a wide array of visual effect parameters ( Rep_VE_* ) for synchronized clientside animations. 

### **APerformanceUnit** 

1. **Purpose** : Manages visibility, Fog of War integration, and shared visual UI elements for performance optimization. 

2. **Implementation (CPP Analysis)** : 

   - ComputeLocalVisibility() : Implements IMassVisibilityInterface to cull units 

   - based on viewport, Fog of War, and team relationship. 

   - HandleSquadHealthBarVisibility() : Elects a squad leader to display a shared USquadHealthBar while collapsing others to reduce UI draw calls. 

   - FireEffects() : Manages pooled VFX/SFX lifecycles using ActiveNiagara and ActiveAudio maps. 

3. **Blueprint Interface** : 

   - **Properties** : MeleeImpactVFX , DeadVFX . EnableFog , IsVisibleEnemy , bIsInvisible . 

   - **Functions** : CheckHealthBarVisibility() , StopAllEffects() , SpawnDamageIndicator() . 

4. **Component Architecture** : Inherits from AMassUnitBase . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

43/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Replicates visibility flags ( StopVisibilityTick , bIsInvisible ) and impact effect assets/parameters. 

### **APathSeekerBase** 

1. **Purpose** : Foundation for custom pathfinding solutions, specifically tailored for Dijkstra matrix navigation. 

2. **Implementation (CPP Analysis)** : Minimal logic base containing FDijkstraMatrix data structures. 3. **Blueprint Interface** : 

   - **Properties** : DijkstraStartPoint , DijkstraEndPoint , FollowPath , EnteredNoPathFindingArea . 

4. **Component Architecture** : Inherits from APerformanceUnit . 

5. **Network/Replication** : Replicates pathfinding state through inherited properties. 

### **ATransportUnit** 

1. **Purpose** : Logic for container-based unit transportation (loading/unloading units). 

2. **Implementation (CPP Analysis)** : 

   - LoadUnit() : Validates TransportId and space requirements before adding units to the 

   - replicated LoadedUnits array. 

   - UnloadNextUnit() : Timer-driven recursive unloading (interval based). Uses line traces for ground 

   - alignment and NetMulticast to restore unit visibility/collision on all clients. 

   - MulticastApplyLoadEffects() : Disables collision and detection, and notifies UUnitVisualManager to hide unit visuals across the network. 

3. **Blueprint Interface** : 

   - **Properties** : IsATransporter , MaxTransportUnits , TransportId , UnitSpaceNeeded . 

   - **Functions** : LoadUnit() , UnloadAllUnits() . 

4. **Component Architecture** : Extends APathSeekerBase . Proximity-based loading triggered via OnCapsuleOverlapBegin . 

5. **Network/Replication** : Replicates LoadedUnits , MaxTransportUnits , CurrentUnitsLoaded , and IsATransporter . 

### **AWorkingUnitBase** 

1. **Purpose** : Specialized unit logic for workers, focusing on resource extraction and construction. 

2. **Implementation (CPP Analysis)** : 

   - SpawnWorkAreaReplicated() : Authoritative spawning of AWorkArea . Contains complex 

   - snapping math for extensions (None, 1-way, 2-way, 4-way, 8-way) using FMath::Atan2 and RoundToFloat . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

44/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - OnRep_CarryingResourceType() : Synchronizes carried resource visuals via UResourceVisualManager . 

3. **Blueprint Interface** : 

   - **Properties** : ResourcePlace , Base , BuildArea . CarryingResourceType . RepairDistance , RepairHealth . 

   - **Functions** : SpawnWorkAreaReplicated() , StartBuild() . 

4. **Component Architecture** : Inherits from ATransportUnit . 

5. **Network/Replication** : Replicates ResourcePlace , Base , BuildArea , CarryingResourceType , and CurrentDraggedWorkArea . 

### **AUnitBase** 

1. **Purpose** : The core RTS unit class, aggregating combat, navigation, and high-level gameplay systems. 

2. **Implementation (CPP Analysis)** : 

   - SpawnProjectileFromClass() : Unified spawning logic for Actor and Mass projectiles. 

   - Supports "TwinProjectile" offsets and multi-shot spread patterns. 

   - Multicast_RegisterBuildingAsObstacle() : Procedurally generates NavObstacleProxy actors with UNavModifierComponent to block navigation. 

   - OnAttributeChanged() : Real-time GAS attribute change listener that drives healthbar UI 

   - visibility and popups. 

3. **Blueprint Interface** : 

   - **Properties** : UnitIcon , Name . CanAttack , bHoldPosition . SummonedUnitsDataSet . 

   - **Functions** : SpawnUnitsFromParameters() , ApplyFollowTarget() , HandleProjectileImpact() . 

4. **Component Architecture** : 

   - BoxCollisionComponent : Tagged collision for building alignment. 

   - Niagara_A/B : Standard unit effect components. 

5. **Network/Replication** : Extensive replication of combat state ( UnitToChase , FollowUnit ), navigation ( NextWaypoint , RunLocation ), and visual assets ( MeshAssetPath , MeshMaterialPath ). 

### **ASpeakingUnit** 

1. **Purpose** : Narrative-focused unit class for dialogue and localized speech audio. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

45/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - PlaySoundOnce() : Integrates with UStoryTriggerQueueSubsystem for global volume 

   - scaling and UGameplayStatics::SpawnSoundAtLocation . 

   - Tick() : Manages USpeechBubble timer synchronization and audio playback states. 

3. **Blueprint Interface** : 

   - **Properties** : SpeechBubbleWidgetComp , SpeechVolume , Text_Id . 

   - **Functions** : SetSpeechWidgetText() . 

4. **Component Architecture** : Extends AUnitBase . Constructor initializes SpeechBubbleWidgetComp (UWidgetComponent). 

5. **Network/Replication** : Inherited. 

### **AHealingUnit** 

1. **Purpose** : Support unit implementation for restorative mechanics. 

2. **Implementation (CPP Analysis)** : 

   - SetNextUnitToChaseHeal() : Iterative search of UnitsToChase , prioritizing targets with Attributes->GetHealth() < GetMaxHealth() and the lowest absolute value. 

   - SpawnHealActor() : Spawns a AHealingActor proxy to apply restorative GameplayEffects 

   - at a target's location. 

3. **Blueprint Interface** : 

   - **Properties** : HealActorSpawnOffset , HealingActorBaseClass . 

   - **Functions** : SpawnHealActor() , SetNextUnitToChaseHeal() . 

4. **Component Architecture** : Inherits from AUnitBase . 

5. **Network/Replication** : Broadcasts healing events via MultiCastStartHealingEvent . 

### **ABuildingBase** 

1. **Purpose** : Stationary structure class with grid-aware worker distribution and procedural connection logic. 

2. **Implementation (CPP Analysis)** : 

   - SwitchResourceArea() : Advanced worker balancing algorithm. Uses ResourceDistanceMultiplier to filter CloseWorkPlaces and AResourceGameMode for team-based distribution. 

   - SpawnEnergyWall() : Procedural spawning and multicast initialization of AEnergyWall 

   - connections between structures. 

3. **Blueprint Interface** : 

   - **Properties** : IsBase , BeaconRange . ExtensionSnapMethod . EnergyWallClass . 

   - ▸ **Functions** : SetEnergyWallsActive() , IsInBeaconRange() . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

46/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Extends AUnitBase . Sets bIsBuilding = true and CanMove = false in the constructor. 

5. **Network/Replication** : Replicates EnergyWallArray for connected structural networks. 

### **AConstructionUnit** 

1. **Purpose** : Represents a structure in progress, utilizing Mass visual effects for build-phase animations. 

2. **Implementation (CPP Analysis)** : 

   - Visual Build Pipeline: Drives rotation, oscillation, and pulsation effects via Mass FMassVisualEffectFragment , bypassing standard Actor ticks. 

   - ResolveVisualComponent() : Scans actor components for valid primitives to animate during 

   - construction. 

3. **Blueprint Interface** : 

   - **Properties** : Worker , WorkArea . bPulsateScaleDuringBuild . 

   - **Functions** : MulticastStartRotateVisual() , KillConstructionUnit() . 

4. **Component Architecture** : Stationary structure ( CanMove = false ). Inherits from AUnitBase . 

5. **Network/Replication** : Replicates Worker and WorkArea references to synchronize build progress. 

# **Components Technical Documentation** 

### **UStoryTriggerComponent** 

1. **Purpose** : Acts as an interface between actors and the UStoryTriggerQueueSubsystem . Its primary responsibility is to fetch story metadata from a UDataTable and request the subsystem to enqueue a story event based on either a specific row ID or a randomized selection. 

2. **Implementation (CPP Analysis)** : 

   - **Trigger Logic** : ShouldTrigger evaluates a probability check using FMath::FRandRange(0.f, 100.f) against the provided ChancePercent . 

   - **Data Mapping** : BuildQueueItemFromRow uses DataTable>FindRow<FStoryWidgetTable> to retrieve raw data. It manually maps fields such as StoryWidgetClass , StoryText , StoryImage , and audio/material assets into an FStoryQueueItem container. 

   - **Randomization** : BuildQueueItemFromRandomRow utilizes StoryDataTable>GetRowNames() to build an index array and selects a random element via FMath::RandRange . 

   - **Subsystem Integration** : The component retrieves the UStoryTriggerQueueSubsystem from the UGameInstance . It passes this as the TriggeringSource within the queue item, allowing the subsystem to track which actor/component initiated the story event. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

47/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Execution Flow** : TryTriggerRandom or TriggerSpecific are the entry points. If the queueing is successful, it broadcasts OnStoryTriggered . 

3. **Blueprint Interface** : 

   - 

   - **Properties** : 

   - LowerVolume (float): Intended for audio ducking control when the story triggers. 

   - StoryDataTable (UDataTable*): Reference to the table containing FStoryWidgetTable 

   - rows. 

- 

   - **Events** : 

   - OnStoryTriggered : Broadcast when a story is successfully enqueued. 

   - OnStoryFinished : Broadcast meant to be triggered when the story UI/event completes. 

- **Functions** : 

   - TryTriggerRandom(float ChancePercent) : Exposed for logic-based narrative 

   - injections. 

   - TriggerSpecific(FName RowName) : Exposed for scripted sequence triggers. 

#### 4. **Component Architecture** : 

- **Constructor** : Explicitly sets PrimaryComponentTick.bCanEverTick = false to minimize overhead, as the component is entirely event-driven. 

- **Dependencies** : Relies on FStoryWidgetTable and FStoryQueueItem (defined in StoryTriggerActor.h ) and UStoryTriggerQueueSubsystem . 

#### 5. **Network/Replication** : 

- This component does not implement any networking or variable replication. It is designed to run locally, typically on the client that manages the UI and Game Instance. If synchronized story triggers are required, the calling logic (e.g., in an Actor) must handle the RPCs before calling the component's functions. 

# **RTSUnitTemplate AI Controller Technical Documentation** 

### **AUnitControllerBase** 

1. **Purpose** : Acts as the primary AI controller for mobile units, managing the finite state machine (FSM), unit detection, and navigation. 

2. **Implementation (CPP Analysis)** : Uses UnitControlStateMachine to drive behavior based on the UnitData state enum. Navigation is abstracted through MoveToLocationUEPathFindingAvoidance , which utilizes UNavigationSystemV1::FindPathSync and fallback to DirectMoveToLocation for 

https://wiki.teufel-engineering.com/en/rts-unit-template 

48/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

flying units or failed paths. Detection logic in DetectUnitsFromGameMode iterates through RTSGameMode->AllUnits with distance and team filtering. 

3. **Blueprint Interface** : Exposes DetectAndLoseUnits , KillUnitBase , RotateToAttackUnit , and SetUEPathfinding for movement. UPROPERTIES include SightRadius , LoseSightRadius , TickInterval , and RotationSpeed . 

4. **Component Architecture** : Inherits from ADetourCrowdAIController . Constructor initializes PrimaryActorTick.TickInterval . OnPossess caches the controlled unit in MyUnitBase . 

5. **Network/Replication** : Replicates UnitDetectionTimer , NewDetectionTime , and IsUnitDetected via GetLifetimeReplicatedProps . Combat actions use Server 

Reliable RPC CreateProjectile . 

### **ASpeakingUnitControllerBase** 

1. **Purpose** : A structural base class for units that require specialized interaction or localized UI/Dialogue hooks. 

2. **Implementation (CPP Analysis)** : Currently serves as an inheritance layer without unique logic over AUnitControllerBase in the core implementation. 

3. **Blueprint Interface** : Inherits all interface members from AUnitControllerBase . 

4. **Component Architecture** : Inherits from AUnitControllerBase . 

5. **Network/Replication** : Inherits networking model from AUnitControllerBase . 

### **AHealingUnitController** 

1. **Purpose** : Specialized controller for support units focused on maintaining the health of friendly units. 

2. **Implementation (CPP Analysis)** : Overrides the state machine logic in HealingUnitControlStateMachine to prioritize friendly unit detection via SetNextUnitToChaseHeal() . Manages a healing cycle across ChaseHealTarget , Healing , and HealPause states. Uses SpawnHealActor to instantiate the healing effect 

when within IsUnitToChaseInRange . 

3. **Blueprint Interface** : HealingUnitControlStateMachine , ChaseHealTarget , Healing , HealPause , HealRun . 

4. **Component Architecture** : Constructor sets DetectFriendlyUnits = true . 

5. **Network/Replication** : Triggers server-side healing events via ServerStartHealingEvent_Implementation . 

### **AWorkerUnitControllerBase** 

1. **Purpose** : Manages complex task-based logic for worker units, including resource gathering, return-to-base cycles, and building construction. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

49/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : Implements task-specific states in WorkingUnitControlStateMachine such as GoToResourceExtraction , ResourceExtraction , GoToBase , and Build . SpawnWorkResource manages visual 

attachment to sockets and resource node depletion. Build logic handles timer-based construction, culminating in SpawnSingleUnit to instantiate building actors. 

3. **Blueprint Interface** : WorkingUnitControlStateMachine , GoToResourceExtraction , ResourceExtraction , GoToBase , GoToBuild , Build . UPROPERTIES for various arrival 

distances and IdleTime . 

4. **Component Architecture** : Interacts with AResourceGameMode for economy logic and AWorkArea for task locations. 

5. **Network/Replication** : Resource depletion is synced via Multicast_SetScale on resource actors; building spawning is authoritative on the server. 

### **ABuildingControllerBase** 

1. **Purpose** : AI controller for stationary structures that execute abilities and provide automated defense. 

2. **Implementation (CPP Analysis)** : BuildingControlStateMachine focuses on Casting , Attack , and Pause states for stationary units. AutoExecuteAbilitys facilitates automatic 

ability triggers based on AutoExeAbilitysArray using an ExecutenDelayTime timer. 

3. **Blueprint Interface** : BuildingControlStateMachine , CastingUnit , AutoExecuteAbilitys , BuildingChase , AttackBuilding . UPROPERTIES: AutoExeAbilitysArray , ExecutenDelayTime . 

4. **Component Architecture** : Controls ABuildingBase actors; navigation components are typically bypassed or restricted. 

5. **Network/Replication** : Uses GAS (Gameplay Ability System) standard replication for ability execution; state changes are authoritative. 

### **ACameraUnitController** 

1. **Purpose** : Utility controller for units representing camera points or simple path-following entities with minimal FSM requirements. 

2. **Implementation (CPP Analysis)** : Implements a simplified CameraUnitControlStateMachine focusing on Run , Idle , and Casting . CameraUnitRunUEPathfinding provides basic coordinate-based navigation. 

3. **Blueprint Interface** : CameraUnitRunUEPathfinding , CameraUnitControlStateMachine . 

4. **Component Architecture** : Minimalist; caches ControllerBase for player-related context. 

5. **Network/Replication** : Standard movement and state replication inherited from base classes. 

**Controller Input Technical Documentation** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

50/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **FTaggedInputAction** 

1. **Purpose** : Data structure for mapping a Gameplay Tag to an Enhanced Input Action asset. 

2. **Implementation (CPP Analysis)** : A USTRUCT that pairs a UInputAction pointer with a FGameplayTag . It serves as the primary data entry type for input configurations. 

3. **Blueprint Interface** : 

   - InputAction : EditDefaultsOnly pointer to a UInputAction . 

   - InputTag : EditDefaultsOnly FGameplayTag . 

4. **Component Architecture** : Standard reflection-enabled struct used within UInputConfig . 

5. **Network/Replication** : Not replicated; used for local client-side input mapping. 

### **UInputConfig** 

1. **Purpose** : Data Asset that stores a collection of input-to-tag mappings. 

2. **Implementation (CPP Analysis)** : 

   - FindInputActionForTag : Logic involves a linear search through the TaggedInputActions array. It validates the pointer and compares tags, returning the first valid 

   - match. 

3. **Blueprint Interface** : 

   - TaggedInputActions : TArray<FTaggedInputAction> exposed for editor 

   - configuration. 

4. **Component Architecture** : Inherits from UDataAsset , facilitating persistent, shared configuration across the project. 

5. **Network/Replication** : None. Standard asset behavior. 

### **UAssetManagerBase** 

1. **Purpose** : Project-specific Asset Manager for handling initial system loading and global access. 

2. **Implementation (CPP Analysis)** : 

   - Get() : Provides static access to the manager via static_cast of the UAssetManager 

   - singleton. 

   - StartInitialLoading() : Overrides the engine lifecycle to trigger FGameplayTags::InitializeNativeTags() , ensuring tags are ready before other objects 

   - initialize. 

3. **Blueprint Interface** : Default Unreal Asset Manager interface. 

4. **Component Architecture** : Singleton pattern inheriting from UAssetManager . 

5. **Network/Replication** : None. Handles local application lifecycle and asset indexing. 

### **FGameplayTags** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

51/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Centralized registry for native Gameplay Tags associated with input events. 

2. **Implementation (CPP Analysis)** : 

   - InitializeNativeTags() : Interacts with UGameplayTagsManager to register all 

   - hardcoded tags. 

   - AddAllTags() : Defines the logic for registering specific tags for clicks, modifiers (Ctrl, Alt, Shift), 

   - movement (WASDQE), actions (R, F, C, G, T, P, O), and UI (Esc, F1-F6). 

   - AddTag() : Internal helper using UGameplayTagsManager::AddNativeGameplayTag 

   - to create tags with a "(Native)" comment prefix. 

3. **Blueprint Interface** : Exposes various FGameplayTag members for C++ access (e.g., InputTag_LeftClick_Pressed ). 

4. **Component Architecture** : Static singleton instance GameplayTags initialized at engine startup. 

5. **Network/Replication** : Native tags are consistent across server and client as they are defined in code. 

### **UEnhancedInputComponentBase** 

1. **Purpose** : Specialized Input Component that allows binding functions to input actions via Gameplay Tags rather than direct asset references. 

2. **Implementation (CPP Analysis)** : 

   - BindActionByTag : A template function that accepts a UInputConfig and a FGameplayTag . It looks up the associated UInputAction and performs a standard BindAction . 

   - Supports passing a CamState integer to the bound function, allowing for state-dependent input processing. 

3. **Blueprint Interface** : Inherits functionality from UEnhancedInputComponent . 

4. **Component Architecture** : Extension of the Enhanced Input system designed for decoupled input management. 

5. **Network/Replication** : Local component; processes hardware input on the client. Resulting actions must be communicated to the server via external RPCs if state changes are required. 

# **RTS Player Controller Technical Documentation** 

### **AControllerBase** 

1. **Purpose** : Core RTS player controller providing base unit selection state, input modifier tracking, and coordinate-based waypoint management for both Dijkstra and UE pathfinding. 

2. **Implementation (CPP Analysis)** : 

   - **Formation Logic** : ComputeGridSize and CalculateGridOffset generate relative offsets for unit placement. RunUnitsAndSetWaypoints iterates through selected units to assign these 

https://wiki.teufel-engineering.com/en/rts-unit-template 

52/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

locations. 

   - **Spatial Tracing** : TraceRunLocation utilizes LineTraceSingleByObjectType against ECC_WorldStatic to project orders onto the landscape, specifically checking for ANavModifierVolume to invalidate orders in non-navigable areas. 

   - **State Management** : Uses SetUnitState_Replication (Server) and SetUnitState_Multi (Multicast) to synchronize unit behavior enums across the network. 

   - **Pathfinding Integration** : Bridges the HUD-level Dijkstra results into unit movement arrays ( RunLocationArray ). 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : SelectedUnits (TArray), UseUnrealEnginePathFinding (Bool), GridSpacing (Formation density), SelectableTeamId (Team ownership). 

   - **UFUNCTIONS** : ShiftPressed/Released , TPressed (Attack Toggle), JumpCamera , SelectUnit . 

#### 4. **Component Architecture** : 

- Constructor configures basic RTS interaction: bShowMouseCursor = true , DefaultMouseCursor = Crosshairs . 

- InitCameraHUDGameMode performs critical linkage between Pawn (as ACameraBase ), HUD (as APathProviderHUD ), and GameMode . 

#### 5. **Network/Replication** : 

- Replicates input states ( IsShiftPressed , IsCtrlPressed , AttackToggled ) and CameraBase reference. 

- Utilizes Server RPCs for authoritative movement ( MoveToLocationUEPathFinding ) and Multicast for cosmetic sync ( Multi_SetBuildingWaypoint ). 

### **AWidgetController** 

1. **Purpose** : Handles UI-to-Logic transactions for unit progression, level data persistence, and team-based resource management. 

2. **Implementation (CPP Analysis)** : 

   - **Unit Mutation** : Loops through SelectedUnits or scans RTSGameMode->AllUnits by UnitIndex or TalentTag to apply state changes. 

   - **Investment Logic** : HandleInvestmentUnitByTagServer_Implementation uses a lambda-based dispatch pattern to apply attribute increments (Stamina, Haste, Armor, etc.) across unit groups. 

   - **Resource Bridging** : Interfaces with AResourceGameMode to poll or modify primary/secondary/tertiary resources via UGameplayStatics::GetGameMode . 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

53/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **UFUNCTIONS** : SaveLevel , LevelUp , ResetTalents , ModifyResource , AddWorkerToResource . All primary mutations are Server, Reliable RPCs. 

4. **Component Architecture** : 

   - Inherits from AControllerBase . Relies on unit-level functions like LoadAbilityAndLevelData for serialization. 

5. **Network/Replication** : 

   - Strictly enforces Server-authoritative resource and attribute modifications to prevent client-side data tampering. 

### **AExtendedControllerBase** 

1. **Purpose** : Manages complex RTS building placement (WorkAreas), hierarchical snapping systems, Energy Wall connections, and Ability Indicators. 

#### 2. **Implementation (CPP Analysis)** : 

   - **WorkArea Dragging** : MoveWorkArea_Local uses raycasting constrained to NavMesh ( ProjectPointToNavigation ). It employs ComputeGroundedLocation to ensure building foundations sit correctly on the landscape. 

   - **Snapping Algorithm** : SnapToActor implements axis-aligned snapping. It calculates building footprints via capsule radii or mesh bounds and uses UKismetSystemLibrary::BoxOverlapActors for pre-placement collision validation. 

   - **Wall Connectivity** : TryConnectEnergyWall and WallTrace manage the logic for connecting buildings. WallTrace specifically filters out the initiator, target, and attached actors to detect real geometry obstructions. 

   - **Mass Integration** : BatchSetRotateToMouseTagLocally manipulates Mass Entity tags ( FMassRotateToMouseTag ) for high-performance unit rotation towards the cursor. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : SnapGap , SnapDistance , EnergyWallSnapZTolerance , ExtensionGroundZThreshold . 

   - **UFUNCTIONS** : SetWorkArea , TryConnectEnergyWall , SelectUnitsWithTag . 

4. **Component Architecture** : 

   - Inherits from AWidgetController . 

   - Subscribes to UMassSignalSubsystem for resource extraction signals to drive UpdateExtractionSounds . 

5. **Network/Replication** : 

   - Replicates ReplicatedMouseLocation for non-owning client ability visualization. 

   - Uses Server_FinalizeWorkAreaPosition to commit ghost placements to the authoritative simulation. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

54/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **ACustomControllerBase** 

1. **Purpose** : High-level RTS coordinator managing optimal group movement, formation assignments, and visual systems (Fog of War/Minimap). 

2. **Implementation (CPP Analysis)** : 

   - **Hungarian Algorithm** : SolveHungarian provides an _O_ ( _n_ 3) solution to the linear assignment problem, ensuring units are matched to formation slots that minimize total squared travel distance. 

   - **Batch Movement** : Batch_CorrectSetUnitMoveTargets optimizes network traffic by grouping move orders. It handles local client-side prediction ( Client_Predict_Batch_CorrectSetUnitMoveTargets ) to hide latency. 

   - **Vision Systems** : UpdateFogMaskWithCircles maps Mass Entity positions to AFogActor texture updates. UpdateMinimap performs similar mapping for the UI minimap. 

   - **Formation Validation** : ValidateAndAdjustGridLocation iteratively searches for valid NavMesh space to fit a group formation, shifting or shrinking spacing as necessary. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : NavMeshProjectionExtent , MainHUDs (TArray of widget classes). 

   - **UFUNCTIONS** : RightClickPressedMass , LeftClickPressedMass , SetHoldPositionOnSelectedUnits . 

4. **Component Architecture** : 

   - Inherits from AExtendedControllerBase . 

   - Manages references to SelectionCircleActor and MinimapActor . 

5. **Network/Replication** : 

   - Implements sophisticated "Movement Prediction" where clients add FMassStateRunTag and FMassClientPredictionFragment immediately, allowing processors to react before the 

   - server's MoveTarget replicates. 

### **ACameraControllerBase** 

1. **Purpose** : Dedicated camera controller for state-driven RTS navigation, unit focus logic, and networksynchronized loading sequences. 

2. **Implementation (CPP Analysis)** : 

   - **State Machine** : CameraBaseMachine handles transitions between UseScreenEdges , MoveWASD , OrbitAndMove , and LockOnSpeaking states. 

   - **Sync Logic** : Server_UpdateCameraUnitMovement throttles network traffic by moving the "Camera Unit" (a physical entity representing the camera focus) using CorrectSetUnitMoveTarget at a configurable interval. 

   - **Initialization Retry** : Retry_ShowLoadingWidget uses a timer loop to ensure widgets are only added once ULocalPlayer and ViewportClient are ready after map travel. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

55/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Math Helpers** : CalculateUnitsAverage determines the geometric center of unit clusters for the automatic camera tracking mode. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : CameraUnitUpdateInterval , OrbitPositions (TArray), UnitZoomScaler . 

   - **UFUNCTIONS** : SetCameraState , Server_TravelToMap , ToggleLockCamToCharacter , ZoomIn/Out . 

4. **Component Architecture** : 

   - Inherits from ACustomControllerBase . Operates primarily on the ACameraBase pawn. 

5. **Network/Replication** : 

   - Server_SyncCameraPosition provides unreliable, high-frequency position updates to the 

   - server for non-owning client camera visualization. 

   - Manages bServerTravelInProgress guard to prevent race conditions during map transitions. 

# **Core Technical Documentation** 

### **UTalentSaveGame** 

1. **Purpose** : Manages the persistence of character progression, attributes, and ability configurations within the SaveGame system. 

2. **Implementation (CPP Analysis)** : 

   - Inherits from USaveGame . 

   - PopulateAttributeSaveData(UAttributeSetBase* AttributeSet) : 

   - Implements a manual mapping of GAS (Gameplay Ability System) attributes to the FAttributeSaveData struct. It utilizes the standard GAS getter pattern (e.g., GetHealth() ) 

   - to extract values from the provided AttributeSet and store them in POD (Plain Old Data) format for serialization. 

3. **Blueprint Interface** : 

   - PopulateAttributeSaveData : Exposed as BlueprintCallable for use in save-flow 

   - logic. 

   - LevelData , LevelUpData , AttributeSaveData : VisibleAnywhere properties 

   - allowing observation of current saved state. 

   - OffensiveAbilityID , DefensiveAbilityID , AttackAbilityID , ThrowAbilityID : Enum-based ability slots for character loadouts. 

4. **Component Architecture** : standard Unreal Engine USaveGame object. 

5. **Network/Replication** : Persistence is typically handled server-side or locally; the class itself is not replicated over the network but its data is often used to initialize replicated attributes on spawn. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

56/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **UResourceVisualConfig** 

1. **Purpose** : A Data Asset providing a centralized mapping of resource types to visual representations. 

2. **Implementation (CPP Analysis)** : 

   - 

      - Inherits from UDataAsset . 

   - Uses a TMap<EResourceType, UStaticMesh*> for efficient mesh lookups based on resource enums. 

3. **Blueprint Interface** : 

   - DefaultResourceMeshes : EditAnywhere and BlueprintReadWrite , enabling 

   - designers to define resource visuals globally. 

4. **Component Architecture** : Standalone Data Asset referenced by resource actors or worker units. 

5. **Network/Replication** : Static configuration asset; loaded locally on all clients. 

### **FCollisionUtils** 

1. **Purpose** : Static utility class providing advanced collision calculations for RTS units, specifically for finding surface impact points on varying component shapes. 

2. **Implementation (CPP Analysis)** : 

   - FindTaggedBoxComponent : Iterates through an actor's components to locate a UBoxComponent tagged with AUnitBase::BoxCollisionTag . 

   - ComputeImpactSurfaceXY : 

      - Calculates the precise 2D impact point on a target's collision boundary. 

      - For UBoxComponent : Uses InverseTransformPosition to move the attacker's location into local space, clamps to box extents, pushes internal points to the nearest edge, and transforms back to world space. 

      - For Capsule/Fallback: Calculates a radial offset based on GetScaledCapsuleRadius (including AdditionalCapsuleRadius for Mass entities) or actor bounds. 

      - Handles Z-axis positioning based on the IsFlying status of both attacker and target. 

3. **Blueprint Interface** : Native C++ utility; functions are static and not explicitly exposed as UFUNCTIONS in this header. 

4. **Component Architecture** : Stateless utility class. 

5. **Network/Replication** : N/A (Utility logic). 

### **FAttributeSaveData** 

1. **Purpose** : A serializable structure for storing current GAS attribute values. 

2. **Implementation (CPP Analysis)** : USTRUCT containing float representations of all unit attributes (Health, Shield, Damage, Range, Haste, Resistance, etc.). 

3. **Blueprint Interface** : All properties are VisibleAnywhere . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

57/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Nested within UTalentSaveGame . 

5. **Network/Replication** : Serialized to disk via the SaveGame system. 

### **FGridData** 

1. **Purpose** : Defines the geometric and dimensional properties of a pathfinding grid. 

2. **Implementation (CPP Analysis)** : USTRUCT inheriting from FTableRowBase for DataTable integration. 

3. **Blueprint Interface** : RowCount , ColCount , Delta (step size), and Offset . 

4. **Component Architecture** : Used as a row in pathfinding configuration tables. 

5. **Network/Replication** : N/A. 

### **FPathMatrixRow** 

1. **Purpose** : Represents a directed edge or connection between two nodes in a Dijkstra pathfinding graph. 

2. **Implementation (CPP Analysis)** : Stores node IDs, 3D coordinates ( FVector3d ), pre-calculated Distance , and a Processed flag for algorithm state tracking. 

3. **Blueprint Interface** : Standard data properties; used primarily in native pathfinding. 

4. **Component Architecture** : Element of FPathMatrix . 

5. **Network/Replication** : N/A. 

### **FDijkstraRow** 

1. **Purpose** : Stores the results and traversal state for a specific node during Dijkstra execution. 

2. **Implementation (CPP Analysis)** : Maps an Id_End to its Id_Previous node and cumulative Costs (uint64). 

3. **Blueprint Interface** : Data storage for path reconstruction. 

4. **Component Architecture** : Element of FDijkstraMatrix . 

5. **Network/Replication** : N/A. 

### **FDijkstraMatrix** 

1. **Purpose** : A collection of Dijkstra results for a specific source node. 

2. **Implementation (CPP Analysis)** : Contains an Id (source node), a CenterPoint , and a TArray<FDijkstraRow> representing the shortest paths to all other reachable nodes. 

3. **Blueprint Interface** : Native data structure. 

4. **Component Architecture** : Data container. 

5. **Network/Replication** : N/A. 

### **FBuildingCost** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

58/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Defines the resource requirements for construction or recruitment. 

2. **Implementation (CPP Analysis)** : 

   - ToFormattedString() : A helper method that generates a multiline string describing non-zero 

   - costs (Primary through Legendary). 

3. **Blueprint Interface** : EditAnywhere integer properties for all resource tiers. 

4. **Component Architecture** : Used in FUnitSpawnParameter and FAbilityCostData . 

5. **Network/Replication** : N/A. 

### **FAbilityCostData** 

1. **Purpose** : Maps a specific Gameplay Ability to its resource cost. 

2. **Implementation (CPP Analysis)** : USTRUCT pairing a 

   - TSubclassOf<UGameplayAbilityBase> with a FBuildingCost . 

3. **Blueprint Interface** : AbilityClass and CurrentCost properties. 

4. **Component Architecture** : Used for UI and validation in ability systems. 

5. **Network/Replication** : N/A. 

### **FSpeechData_Texts** 

1. **Purpose** : Configures dialogue and speech parameters for units. 

2. **Implementation (CPP Analysis)** : Inherits from FTableRowBase . Includes text, associated sound assets, blend points for facial animation, and display timing. 

3. **Blueprint Interface** : Text (MultiLine), SpeechSound , BlendPoint_1/2 , and Time . 

4. **Component Architecture** : DataTable row. 

5. **Network/Replication** : N/A. 

### **FSpeechData_Buttons** 

1. **Purpose** : Defines interactive dialogue choices. 

2. **Implementation (CPP Analysis)** : Inherits from FTableRowBase . Maps a choice to a specific text ID and defines the New_Text_Id for dialogue branching. 

3. **Blueprint Interface** : Text_Id , New_Text_Id , Text , and ButtonSound . 

4. **Component Architecture** : DataTable row. 

5. **Network/Replication** : N/A. 

### **FLevelData** 

1. **Purpose** : Tracks a unit's current level, experience, and available skill points. 

2. **Implementation (CPP Analysis)** : Stores current Experience , CharacterLevel , and tracking for both available and used Talent/Ability points. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

59/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

3. **Blueprint Interface** : BlueprintReadOnly properties for UI integration. 

4. **Component Architecture** : Member of UTalentSaveGame . 

5. **Network/Replication** : N/A. 

### **FLevelUpData** 

1. **Purpose** : Configuration asset for tuning the character progression curve. 

2. **Implementation (CPP Analysis)** : Defines static rules like ExperiencePerLevel , MaxCharacterLevel , and reward frequency (e.g., AbilityPointsEveryXLevel ). 

3. **Blueprint Interface** : EditAnywhere tuning parameters. 

4. **Component Architecture** : Used by progression logic to calculate level-ups. 

5. **Network/Replication** : N/A. 

### **FUnitSpawnParameter** 

1. **Purpose** : Comprehensive configuration for unit instantiation. 

2. **Implementation (CPP Analysis)** : Inherits from FTableRowBase . Defines class, count, spatial ranges, initial UnitData::EState , visual overrides (Mesh/Material), and squad grouping logic. 

3. **Blueprint Interface** : Extensive property list including UnitBaseClass , SpawnAsSquad , and CanBeSelected . 

4. **Component Architecture** : Used as the primary definition for spawning systems and recruitment queues. 

5. **Network/Replication** : N/A. 

### **FUnitSpawnData** 

1. **Purpose** : A runtime container for a spawned unit and its source parameters. 

2. **Implementation (CPP Analysis)** : Pairs a live AUnitBase* reference with its original FUnitSpawnParameter . 

3. **Blueprint Interface** : UnitBase and SpawnParameter . 

4. **Component Architecture** : Used for tracking active units. 

5. **Network/Replication** : N/A. 

### **FResourceArray** 

1. **Purpose** : Manages multiple resource pools and worker allocation for a specific resource type. 

2. **Implementation (CPP Analysis)** : 

   - Custom constructor initializes parallel arrays ( Resources , CurrentWorkers , MaxWorkers , MaxResources ) to a specific size. 

3. **Blueprint Interface** : VisibleAnywhere arrays for monitoring resource nodes. 

4. **Component Architecture** : Used in resource extraction logic. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

60/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : N/A. 

### **FWorkResourceVisuals** 

1. **Purpose** : Configuration for resource-related visual components. 

2. **Implementation (CPP Analysis)** : Defines UStaticMesh , UMaterialInterface , Scale , and SocketOffset for resource nodes or worker attachments. 

3. **Blueprint Interface** : EditAnywhere visual properties. 

4. **Component Architecture** : Data structure used by worker units to dynamically update their appearance based on gathered resources. 

5. **Network/Replication** : N/A. 

# **GAS Module Technical Documentation** 

### **UAbilitySystemComponentBase** 

1. **Purpose** : Specialized Ability System Component for the RTS template, extending UAbilitySystemComponent to serve as the core component for units and players participating in 

the Gameplay Ability System. 

2. **Implementation (CPP Analysis)** : Inherits all base functionality from UAbilitySystemComponent . It acts as the primary interface for granting UGameplayAbilityBase instances and managing the UAttributeSetBase or UResourceAttributeSet associated with the owner. 

3. **Blueprint Interface** : Exposed via UCLASS() , allowing designers to add this component to Actor Blueprints. 

4. **Component Architecture** : Standard Unreal Component setup; meant to be created as a default subobject in an Actor's constructor. 

5. **Network/Replication** : Inherits robust replication for GameplayTags, GameplayEffects, and GameplayAbilities from the base GAS component. 

### **UGameplayAbilityBase** 

1. **Purpose** : An enhanced base class for RTS-specific abilities, incorporating economic costs, global/local ability gating, UI metadata, and Mass Entity synchronization. 

2. **Implementation (CPP Analysis)** : 

   - **Ability Gating** : Implements a static registry system ( GDisabledAbilityKeysByTeam , GForceEnabledAbilityKeysByOwner , etc.) to enable/disable abilities globally by string 

   - keys. CanActivateAbility checks these registries in order: Owner Force > Owner Disable > Team Force > Asset bDisabled > Team Disable. 

   - **Mass Sync** : In ActivateAbility and EndAbility , if bRotateUnitsToMouse is true, it manually updates FTransformFragment and 

https://wiki.teufel-engineering.com/en/rts-unit-template 

61/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

FMassAgentCharacteristicsFragment to ensure the unit's visual representation in Mass matches its Gameplay rotation. 

   - **Resource Logic** : Integrates FBuildingCost and handles refunds via AResourceGameMode if an ability is cancelled and bRefundOnCancel is true. 

   - **Sound** : PlayOwnerLocalSound ensures sounds are played locally for the owning player while specifically filtering out AI agents ( ARLAgent ) to avoid ghost audio from automated units. 

   - **Unit Upgrades** : UpgradeUnits uses a static map GActiveUpgradesByTeam to apply UGameplayEffect to current and future units matching specific FGameplayTag criteria. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : AbilityIcon , ConstructionCost , AbilityKey , AbilityInputID , bDisabled , bRotateUnitsToMouse . 

   - **UFUNCTIONS** : PlayOwnerLocalSound , SpawnProjectileFromClass , SetAbilitiesEnabledForTeamByKey , UpgradeUnits . 

4. **Component Architecture** : Constructor initializes the ToolTipText based on name, cost, and hotkey. 

5. **Network/Replication** : Leverages ACustomControllerBase RPCs to synchronize ability key states (Enabled/Disabled) between server and clients. 

### **UAttributeSetBase** 

1. **Purpose** : Manages the combat and movement statistics for RTS units, including health, shields, damage, speed, and various RPG-style attributes. 

2. **Implementation (CPP Analysis)** : 

   - **PostGameplayEffectExecute** : Implements custom damage handling logic. EffectDamage magnitude is applied first to Shield . If damage exceeds shield, the remainder is applied to Health . 

   - **Threshold Notifications** : During damage or healing, it calculates health percentages and triggers UnitBase->OnHealthThresholdCrossed at 25% and 50% benchmarks. 

   - **Clamping Logic** : SetAttributeHealth and SetAttributeShield ensure values stay within [0, Max] and manage unit state transitions (e.g., calling DeadEffectsAndEvents when health reaches zero). 

   - **Visual Feedback** : Automatically calls SpawnIndicator to display damage (Red), healing (Green), or shield (Blue) numbers over the unit. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : Health , Shield , MaxHealth , AttackDamage , RunSpeed , Range , Armor , MagicResistance . 

   - **UFUNCTIONS** : UpdateAttributes , SetAttributeHealth , SetAttributeShield , plus individual attribute setters. 

4. **Component Architecture** : Uses the ATTRIBUTE_ACCESSORS macro for standard GAS boilerplate. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

62/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : All attributes are replicated via DOREPLIFETIME_CONDITION_NOTIFY with REPNOTIFY_Always . OnRep functions use GAMEPLAYATTRIBUTE_REPNOTIFY to maintain 

client-side prediction and synchronization. 

### **UResourceAttributeSet** 

1. **Purpose** : Manages player-level economic data including resource quantities and worker allocation counts. 

2. **Implementation (CPP Analysis)** : A specialized UAttributeSet that tracks six tiers of resources (Primary to Legendary) and corresponding worker counts. It relies on Gameplay Effects to modify these values during resource collection or unit/building construction. 

3. **Blueprint Interface** : 

   - **UPROPERTIES** : PrimaryResource , SecondaryResource , TertiaryResource , RareResource , EpicResource , LegendaryResource . 

   - **UPROPERTIES** : PrimaryWorkers , SecondaryWorkers , TertiaryWorkers , RareWorkers , EpicWorkers , LegendaryWorkers . 

4. **Component Architecture** : Uses ATTRIBUTE_ACCESSORS macro; typically added to the PlayerState or a global team manager Actor. 

5. **Network/Replication** : Uses REPNOTIFY_Always for all attributes to ensure all clients on the same team see up-to-date economic status. 

# **GameInstances Technical Documentation** 

### **URTSGameInstance** 

1. **Purpose** : Acts as the high-level manager for persistent game state and global logic that must survive level transitions within the RTS Template. It serves as the primary entry point for global systems that do not belong to specific actors or levels. 

2. **Implementation (CPP Analysis)** : 

   - Inherits from UGameInstance . 

   - Currently utilizes default Unreal Engine UGameInstance lifecycle methods. 

   - The implementation file ( RTSGameInstance.cpp ) includes the header and provides a stub for future global logic, such as session management or global setting initialization. 

3. **Blueprint Interface** : 

   - Class is marked with UCLASS() , making it available for Blueprint subclassing. 

   - No specific UPROPERTY or UFUNCTION members are currently exposed in the provided source. 

4. **Component Architecture** : 

   - Constructor follows standard Unreal GENERATED_BODY() patterns. 

   - No sub-objects or components are initialized in the current implementation. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

63/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

#### 5. **Network/Replication** : 

- As a UGameInstance , this object is not replicated. Each client and the server have their own local instance. 

- Used for storing local player data or handling client-side transition logic that does not require network synchronization via the actor replication system. 

# **GameModes Technical Deep-Dive Documentation** 

This document provides a technical analysis of the GameMode hierarchy in the RTSUnitTemplate, detailing the orchestration of session lifecycle, resource management, and research systems. 

### **ARTSGameModeBase** 

1. **Purpose** : Acts as the primary orchestrator for the RTS session, managing global unit registries, team initialization via PlayerStarts, win/lose condition evaluation, and data-driven unit spawning. 

2. **Implementation (CPP Analysis)** : 

   - **Session Lifecycle** : BeginPlay initializes tag tracking maps ( TagsDestroyedCountMap , etc.) and triggers FillUnitArrays . It schedules SetTeamIdsAndWaypoints via a timer to allow late-joining controllers to settle. 

   - **Team Assignment** : SetTeamIdsAndWaypoints_Implementation maps ACameraControllerBase instances to APlayerStartBase actors. It checks the UPlayerTeamSubsystem for lobby-assigned teams and falls back to PlayerStart settings. For 

   - unoccupied AI starts, it spawns an AI PC, a Pawn, and an ARTSBTController orchestrator. 

   - **Win/Lose Evaluation** : CheckWinLoseCondition performs a full world scan using TActorIterator<ASpawnerUnit> to update alive tag counts. It evaluates AWinLoseConfigActor step-based conditions, including building counts, tag counts, match time, 

   - and resource levels. 

   - **Data-Driven Spawning** : SpawnUnits_Implementation interprets FUnitSpawnParameter from DataTables. It uses UGameplayStatics::BeginDeferredActorSpawnFromClass to allow mesh and 

   - material overrides before finishing spawning. It manages SquadId assignment and global unit indexing via HighestUnitIndex . 

   - **Nav Warmup** : NavInitialisation executes a synchronous pathfinding query between two random reachable points to ensure the UNavigationSystemV1 is fully initialized before AI starts. 

3. **Blueprint Interface** : 

   - **Properties** : AIPlayerPawnClass , AIPlayerControllerClass , AIOrchestratorClass , AIBehaviorTree , UnitSpawnParameters , GatherControllerTimer . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

64/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ **Functions** : SpawnUnitFromDataTable , CheckAndRemoveDeadUnits , IsPathfindingRdy , SetupTimerFromDataTable . 

4. **Component Architecture** : Inherits from AGameModeBase . It interacts heavily with AResourceGameState for global data synchronization and ACameraControllerBase for 

player-specific commands. 

5. **Network/Replication** : 

   - Replicates TimerIndex , AllUnits , and CameraUnits via GetLifetimeReplicatedProps . 

   - Utilizes Client RPCs like Client_ShowLoadingWidget and Client_TriggerWinLoseUI to sync state transitions to non-authoritative clients. 

   - Spawning logic is server-authoritative via Server reliable RPCs. 

### **AResourceGameMode** 

1. **Purpose** : Specializes the game mode to handle a resource-based economy, including resource modification logic and sophisticated worker assignment heuristics. 

2. **Implementation (CPP Analysis)** : 

   - **Resource Logic** : ModifyResource_Implementation handles the arithmetic of the TeamResources array. It specifically checks SupplyLikeResources to determine if an 

   - amount should be added or subtracted (representing usage vs. gathering). 

   - **Worker Assignment** : AssignWorkAreasToWorker implements a proximity-based assignment using a DistanceThreshold derived from ResourceDistanceMultiplier . It respects IsWorkerDistributionSet to balance workers across resource types using GetCurrentWorkersForResourceType vs GetMaxWorkersForResourceType . 

   - **Area Indexing** : GatherWorkAreas uses TActorIterator<AWorkArea> to sort resource nodes into the FWorkAreaArrays struct based on their WorkAreaData type (Primary, Secondary, etc.). 

   - **Affordability** : CanAffordConstruction iterates through TeamResources and compares against FBuildingCost , with specific handling for supply-cap logic. 

3. **Blueprint Interface** : 

   - **Properties** : ResourceDistanceMultiplier , MaxResourceAreasToSet , SupplyLikeResources , TeamResources . 

   - **Functions** : ModifyResource , ModifyMaxResource , CanAffordConstruction , AssignWorkAreasToWorker , SetAllCurrentWorkers . 

4. **Component Architecture** : Inherits from ARTSGameModeBase . Integrates the FWorkAreaArrays storage for spatial queries. 

5. **Network/Replication** : 

   - Replicated members: NumberOfTeams , TeamResources . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

65/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

- Uses Server RPCs ( ModifyResource , ModifyMaxResource ) to ensure resource transactions are verified on the authority. 

### **AUpgradeGameMode** 

1. **Purpose** : Manages the persistent research state for all teams, initializing tech trees and handling upgrade progression. 

2. **Implementation (CPP Analysis)** : 

   - **Tech Tree Init** : InitializeUpgradesForTeams populates the AUpgradeGameState with standard upgrade sets (e.g., "Robotic Cleave", "Tank Health") for up to 8 teams during BeginPlay . 

   - **Research Execution** : ResearchUpgrade locates the FUpgradeStatus in the TeamUpgradesArray by name and sets Researched = true . It uses MarkItemDirty to trigger efficient networking through the FTeamUpgrades fast array 

   - serializer. 

3. **Blueprint Interface** : 

   - **Functions** : InitializeUpgradesForTeams , AddUpgrade , ResearchUpgrade , InitializeSingleUpgrade . 

4. **Component Architecture** : Inherits from AResourceGameMode , leveraging the existing team and resource structures. 

5. **Network/Replication** : While the logic resides in the GameMode (Server-only), the state is maintained in AUpgradeGameState which replicates the TeamUpgradesArray to all clients. 

# **GameStates Technical Documentation** 

### **AResourceGameState** 

1. **Purpose** : Acts as the central authority for global match resources and session state management. It tracks resource pools across teams and handles the synchronization of match start sequences and UI loading states. 

2. **Implementation (CPP Analysis)** : 

   - **Replication Setup** : GetLifetimeReplicatedProps registers TeamResources , IsSupplyLike , LoadingWidgetConfig , MatchStartTime , and bStartupFreezeReleased . 

   - **UI Synchronization** : OnRep_LoadingWidgetConfig is triggered on clients. It iterates through the world's PlayerControllerIterator , specifically targeting the local player controller (via IsLocalPlayerController() ) and calling CheckForLoadingWidget() on the ACameraControllerBase to update the HUD/Loading screen. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

66/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Resource Management** : SetTeamResources allows the server to push raw resource data into the replicated TeamResources array. 

3. **Blueprint Interface** : 

   - 

- **UPROPERTIES** : 

- TeamResources ( TArray<FResourceArray> ): Replicated resources per team. 

- 

   - IsSupplyLike ( TArray<bool> ): Replicated metadata defining resource behavior. 

- LoadingWidgetConfig ( FLoadingWidgetConfig ): Replicated config for UI state. 

- 

      - MatchStartTime ( float ): Global timestamp for session start. 

   - bStartupFreezeReleased ( bool ): Global control flag for unit movement/input availability. 

- **UFUNCTIONS** : 

   - OnRep_TeamResources() : Notify function for resource updates. 

   - 

         - SetTeamResources() : Server-side data setter. 

      - OnRep_LoadingWidgetConfig() : Internal notify for client-side UI logic. 

4. **Component Architecture** : Derived from AGameStateBase . It does not define additional subcomponents in the constructor. 

5. **Network/Replication** : 

   - 

   - Server-authoritative resource distribution. 

- Uses OnRep notifications to ensure late-joining clients or state-changing clients can correctly synchronize transient UI elements (Loading Widgets). 

### **AUpgradeGameState** 

1. **Purpose** : Specializes AResourceGameState to manage technology progression and research status for all participating teams using an efficient replication model. 

2. **Implementation (CPP Analysis)** : 

   - **Optimization** : Utilizes FFastArraySerializer patterns. Functions like SetUpgradeResearched use MarkItemDirty() to replicate only specific item changes 

   - within the struct array, rather than the entire collection. 

   - **Team Mapping** : Uses a 1-based TeamId convention for external calls, which is mapped to a 0- indexed TeamUpgradesArray internally. 

   - **Search Logic** : GetUpgradeInvestmentEffect and GetUpgradeResearchedStatus implement string-based lookups ( ESearchCase::IgnoreCase ) to bridge data-driven design (strings) with internal state. 

   - **Authority Guarding** : Most modification functions (e.g., AddUpgradeToTeam , ResearchUpgradeByName ) check HasAuthority() to ensure state integrity is maintained 

   - on the server. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

67/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

#### 3. **Blueprint Interface** : 

- 

   - **UPROPERTIES** : 

   - TeamUpgradesArray ( TArray<FTeamUpgrades> ): Replicated collection of research 

   - states per team. 

- 

- **UFUNCTIONS** : 

- 

- 

   - SetTeamUpgrades() : Bulk initialization of team tech state. 

   - SetUpgradeResearched() : Index-based research status toggle. 

- GetUpgradeInvestmentEffect() : Returns associated UGameplayEffect for 

- specific upgrades. 

- 

      - AddUpgradeToTeam() : Appends new upgrade definitions to a team's pool. 

   - GetUpgradeResearchedStatus() : Queries the status of a specific upgrade by name. 

   - ResearchUpgradeByName() : Toggles research status using string identifiers. 

4. **Component Architecture** : Extends AResourceGameState . Inherits base behavior and focuses on the technology/research domain. 

#### 5. **Network/Replication** : 

- Employs FFastArraySerializer via FTeamUpgrades and FUpgradeStatus structs. 

- Uses MarkArrayDirty() when adding or resizing the team list. 

- Uses MarkItemDirty() for high-frequency updates like researching a single node. 

- OnRep_TeamUpgrades() provides a hook for UI elements to react to broad research changes. 

# **HUD Technical Deep-Dive Documentation AHUDBase** 

1. **Purpose** : Acts as the central visualization and selection hub for the RTS environment. It handles screenspace selection logic (both skeletal and Instanced Static Mesh units), 3D-to-2D projection for UI elements (like movement lines and waypoints), and proximity-based unit interactions. 

#### 2. **Implementation (CPP Analysis)** : 

- **Selection Logic** : DrawHUD implements a marquee selection. It calculates a scaled selection rectangle ( RectangleScaleSelectionFactor ) and uses GetActorsInSelectionRectangle for standard actors. For performance, it projects world 

- locations to screen space to verify containment. 

- **ISM Selection** : SelectISMUnitsInRectangle iterates through AMassUnitBase actors and their FMassUnitVisualFragment . It retrieves instance transforms from UInstancedStaticMeshComponent to perform screen-space AABB tests on individual 

- instances. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

68/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Visualizations** : DrawDashedLine3D projects 3D world segments into 2D screen space using ProjectWorldLocationToScreen . It segments lines based on DashLen and GapLen . 

   - **Waypoint Rendering** : DrawSelectedBuildingWaypointLinks performs line traces ( LineTraceSingleByChannel ) against ECC_WorldStatic to detect terrain clipping, adjusting waypoint links vertically to ensure visibility. 

   - **Logic Loops** : MoveUnitsThroughWayPoints and IsSpeakingUnitClose iterate through unit arrays, calculating Euclidean distances ( sqrt of squared differences) to trigger state changes or UI updates (Speech Bubbles). 

3. **Blueprint Interface** : 

   - **UFUNCTIONS** : SelectISMUnitsInRectangle , DrawDashedLine3D , SetExtensionPreviewLine , DeselectAllUnits , SetUnitSelected , IsSpeakingUnitClose . 

   - **UPROPERTIES** : Extensive configuration for visuals: WPLineColor , UnitWPLineColorMove , ClickIndicatorRadius , RectangleScaleSelectionFactor , bSelectFullSquad . 

4. **Component Architecture** : Inherits from AHUD . It does not define custom sub-components but heavily interacts with UMassEntitySubsystem , UInstancedStaticMeshComponent , and UWidgetSwitcher . 

5. **Network/Replication** : Overrides GetLifetimeReplicatedProps . Selection logic is primarily local, but SelectUnitsFromSameSquad forwards requests to ACameraControllerBase::Server_SelectUnitsFromSameSquad to ensure squad- 

wide state synchronization across the server. 

### **APathProviderHUD** 

1. **Purpose** : Extends AHUDBase to provide a Dijkstra-based pathfinding system. It generates navigation grids from data tables, pre-calculates Dijkstra matrices for specific center points, and provides real-time path refinement. 

2. **Implementation (CPP Analysis)** : 

   - **Grid Generation** : CreatePathMatrix generates a 2D grid of points based on ColCount , RowCount , and Delta . It uses LineTraceSingleByChannel to verify connectivity 

   - between nodes, ignoring units via QueryParams . 

   - **Dijkstra Algorithm** : Dijkstra implements the shortest-path algorithm. It uses a queue-based approach ( DijkstraInit , CheckDijkstraLoop ) to populate FDijkstraRow structures with cost and parent-pointer data. 

   - **Path Reconstruction** : GetDijkstraPath traverses the parent pointers from an EndId back to the start node (Id 1) within MaxPathIteration limits. 

   - **Real-Time Refinement** : GetPathReUseDijkstra combines pre-calculated paths with a local, real-time Dijkstra pass. It performs line-of-sight checks between nodes in the combined path to simplify and optimize the final route. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

69/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Execution Timing** : Uses StartTimer in Tick to delay grid creation 

      - ( CreateGridAndDijkstra ) until the environment is loaded. ControlTimer regulates the frequency of SetNextDijkstra calls to distribute CPU load. 

3. **Blueprint Interface** : 

   - **UFUNCTIONS** : CreateGridAndDijkstra (Manual trigger), SetNextDijkstraTo (Assigns a unit to a navigation matrix based on location), SetDijkstraWithClosestZDistance . 

   - **UPROPERTIES** : GridDataTable (Source for grid specs), MaxCosts , MaxDistance , Debug (Triggers DrawDebugLine and DrawDebugCircle for grid visualization). 

4. **Component Architecture** : Inherits from AHUDBase . Utilizes FGridData rows from a UDataTable to define multiple navigation areas. 

5. **Network/Replication** : Pathfinding calculations are performed on the HUD instance. Results are typically applied to units which then synchronize their movement state via standard movement replication. 

# **Mass Abilitys Technical Documentation** 

This document provides a technical deep-dive into the Mass Abilitys module, detailing the purpose, implementation, and architectural setup for each class within the system. 

### **FMassDecalScalingTag** 

1. **Purpose** : A marker tag used to identify Mass entities that are currently undergoing a decal scaling animation managed by the UMassDecalScalingProcessor . 

2. **Implementation (CPP Analysis)** : Inherits from FMassTag . It contains no data. Its presence in an entity's composition allows the scaling processor to filter and operate on relevant entities without additional logic checks. 

3. **Blueprint Interface** : Defined as a USTRUCT , but typically not interacted with directly via Blueprints other than through Mass Entity Configs or Trait assignments. 

4. **Component Architecture** : Standard Mass Tag structure. No specialized constructor logic. 

5. **Network/Replication** : As a tag, its replication depends on the Mass Entity template's fragment replication settings. It is used locally by processors on both Server and Client to drive visual scaling. 

### **UMassEffectAreaVisualProcessor** 

1. **Purpose** : Manages the visual representation of effect areas, specifically updating Instanced Static Mesh (ISM) transforms and Niagara component states based on entity fragments. 

2. **Implementation (CPP Analysis)** : 

   - **VisualQuery** : Collects active effect areas with FEffectAreaVisualFragment , FEffectAreaImpactFragment , FTransformFragment , FMassActorFragment , 

   - and FMassVisibilityFragment . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

70/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Logic** : In Execute , it calculates the scale factor for the ISM instance by comparing Impact.CurrentRadius with Visual.BaseMeshRadius . It updates the instance 

   - transform using UpdateInstanceTransform . It also handles Niagara component positioning and visibility. 

   - **CleanupQuery** : Identifies entities where FMassEffectAreaActiveTag is missing but FMassEffectAreaImpactTag remains. It zeros out ISM scales, destroys associated actors, and 

   - destroys the Mass entity. 

3. **Blueprint Interface** : None. Logic is entirely internal to the Mass processing pipeline. 

4. **Component Architecture** : Sets ProcessingPhase to PostPhysics . bRequiresGameThreadExecution is true because it interacts with AActor components 

(ISM, Niagara). 

5. **Network/Replication** : Runs on both Server and Client. It synchronizes with the AEffectArea actor to check for FOW visibility ( bIsVisibleByFog ) and replicated triggers like bImpactVFXTriggered . 

### **UChargeMonitorProcessor** 

1. **Purpose** : Monitors entities in a "Charging" state, tracking duration and reverting movement attributes once the charge duration completes. 

2. **Implementation (CPP Analysis)** : 

   - **Timer** : Uses a custom TimeSinceLastRun to throttle execution based on ExecutionInterval . 

   - **Logic** : Increments State.StateTimer . When StateTimer >= ChargeTimer.ChargeEndTime , it reverts MoveTarget.DesiredSpeed and StatsList[i].RunSpeed to the original values stored in the ChargeTimer fragment. It 

   - then removes the charging fragment and tag. 

3. **Blueprint Interface** : ExecutionInterval is BlueprintReadWrite and EditAnywhere . 

4. **Component Architecture** : Executes in the Behavior group, specifically after Tasks . 

5. **Network/Replication** : ExecutionFlags are set to Server . This ensures movement state changes and speed reversions are authoritative. 

### **UMassEffectAreaImpactProcessor** 

1. **Purpose** : High-level controller for effect area lifecycles, radius evolution (scaling/pulsating), and collision/impact logic against unit entities. 

2. **Implementation (CPP Analysis)** : 

   - **Radius Calculation** : Logic handles multiple modes: bIsScalingAfterImpact (Lerp), bPulsate (Sine wave), bIsRadiusScaling (Linear Lerp), or BaseRadius . 

   - **Collision** : Performs a manual radial check using FVector::DistSquared against a list of unit locations gathered in UnitQuery . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

71/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Impact** : Applies UGameplayEffect classes stored in FEffectAreaImpactFragment to units via AUnitBase::ApplyInvestmentEffect . 

   - **Destruction/Spawning** : Manages PostImpactTimer . If server-side, it triggers SpawnUnitsForEffectArea which handles ground tracing and deferred actor spawning for 

   - units upon area destruction. 

3. **Blueprint Interface** : None. Logic is internal. 

4. **Component Architecture** : PostPhysics phase. Requires Game Thread for actor interaction. 

5. **Network/Replication** : Server-only for impact application, unit spawning, and entity removal. Clients synchronize visual-related flags like bIsScalingAfterImpact from the AEffectArea actor. 

### **UEffectAreaVisualManager** 

1. **Purpose** : A world subsystem that provides centralized management for ISM pooling and the registration of visual instances for Mass-driven effect areas. 

2. **Implementation (CPP Analysis)** : 

   - **Pooling** : Uses TMap<FMeshMaterialKey, UInstancedStaticMeshComponent*> ISMPool . GetOrCreatePooledISM creates or retrieves components attached to a ManagerActor . 

   - **Registration** : AddVisualInstance populates FEffectAreaVisualFragment with ISM component pointers and instance indices. It also captures Niagara component references from the AEffectArea actor before cleaning up the actor's template components. 

3. **Blueprint Interface** : None. 

4. **Component Architecture** : UWorldSubsystem . Creates a hidden AActor (labelled "EffectAreaVisualManagerActor" in editor) to own the ISM components. 

5. **Network/Replication** : Standard subsystem behavior. Local instance registration. 

### **UTransportProcessor** 

1. **Purpose** : Coordinates "loading" interactions between transport-capable units and their followers. 

2. **Implementation (CPP Analysis)** : 

   - **Proximity Logic** : Iterates through followers looking for a FriendlyTargetEntity . If the target has a FMassTransportFragment , it checks the 2D distance against InstantLoadRange . 

   - **Signaling** : Uses UMassSignalSubsystem::SignalEntityDeferred with UnitSignals::LoadUnit to trigger the actual load logic on the follower entity. 

   - **Inactivity** : Includes a 30s DeactivationTimer . If a transporter has no followers targeting it, the FMassTransportProcessorActiveTag is eventually removed to optimize performance by 

   - removing the active tag. 

3. **Blueprint Interface** : None. 

4. **Component Architecture** : Behavior group. Server | Standalone execution flags. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

72/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Server-only logic to ensure loading events are authoritative. 

### **UGamePlayEffectProcessor** 

1. **Purpose** : Implements aura-style mechanics where casters apply persistent Gameplay Effects to nearby units. 

2. **Implementation (CPP Analysis)** : 

   - **Caster/Target Split** : Separates entities into CasterQuery (auras) and TargetQuery (receivers). 

   - **Application Logic** : Checks FVector::DistSquared against EffectRadius . Differentiates between friendly and enemy targets to apply specific UGameplayEffect classes via UnitBase->ApplyInvestmentEffect . 

   - **Cooldowns** : Uses FriendlyEffectCoolDown and EnemyEffectCoolDown within the target fragment to prevent frame-by-frame effect re-application. 

3. **Blueprint Interface** : ExecutionInterval is BlueprintReadWrite . 

4. **Component Architecture** : Behavior group, executed after Tasks . Requires Game Thread. 

5. **Network/Replication** : Server | Standalone execution. authoritatively manages effect application on units. 

### **UMassDecalScalingProcessor** 

1. **Purpose** : Synchronizes the visual radius of UAreaDecalComponent with Mass fragments, enabling smooth programmatic scaling of area indicators. 

2. **Implementation (CPP Analysis)** : 

   - **Component Interop** : Finds UAreaDecalComponent on the actor. Calls AdvanceMassScaling , which performs internal interpolation and returns a NewRadius . 

   - **Fragment Sync** : Updates FMassGameplayEffectFragment::EffectRadius with the calculated radius. 

   - **Building Integration** : If the actor is an ABuildingBase , it calls SetBeaconRange to synchronize building logic with the visual decal. 

3. **Blueprint Interface** : ExecutionInterval is EditAnywhere . 

4. **Component Architecture** : PostPhysics phase. Requires Game Thread for actor/component interaction. 

5. **Network/Replication** : EProcessorExecutionFlags::All . Ensures both Server and Clients see consistent decal scaling. 

# **Mass Avoidance Technical Documentation** 

### **UUnitSeparationProcessor** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

73/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Applies lateral repulsion forces between nearby units to prevent clumping while maintaining group flow during movement and combat. 

2. **Implementation (CPP Analysis)** : 

   - **Throttling** : Uses ExecutionInterval to limit processing frequency. 

   - **Logic** : Gathers unit information ( FClumpUnitInfo ) including team IDs, targets, and "bracing" status. 

   - **Math** : Calculates lateral push vectors by finding the "Right" vector relative to a unit's forward direction. The force magnitude is derived from the overlap between units' capsule radii and configurable strength multipliers. 

   - **Unreal-APIs** : Uses UNavigationSystemV1::ProjectPointToNavigation to validate locations on the NavMesh. It checks for FMassSoftAvoidanceTag to prevent units already pushed against walls from being further displaced by other units. 

3. **Blueprint Interface** : 

   - Debug : Visualizes repulsion circles and push vectors. 

   - RepulsionStrengthFriendly/Enemy/Worker : Configurable force magnitudes. 

   - DistanceMultiplierFriendly/Enemy : Scaling factors for separation distance. 

   - MaxCheckRadius : Performance cap for proximity checks. 

4. **Component Architecture** : 

   - **Constructor** : Assigned to UE::Mass::ProcessorGroupNames::Avoidance group. 

   - **Phase** : Runs in EMassProcessingPhase::PrePhysics . 

   - **Requirements** : Accesses FTransformFragment , FMassForceFragment (ReadWrite), FMassAITargetFragment , FMassCombatStatsFragment , FMassAgentCharacteristicsFragment , and FMassMoveTargetFragment . 

5. **Network/Replication** : Flags set for Server | Client | Standalone execution. Forces are calculated locally on each simulation instance. 

### **UUnitMovingAvoidanceProcessor** 

1. **Purpose** : Provides high-fidelity predictive avoidance for moving agents, extending the base Unreal Mass avoidance functionality to handle environment edges and complex agent interactions. 

2. **Implementation (CPP Analysis)** : 

   - **Delayed Start** : Uses AvoidanceStartDelay to prevent avoidance logic from firing immediately upon world start. 

   - **Math** : Implements ComputeClosestPointOfApproach (CPA) using ray-capsule intersection logic to predict future collisions within a time horizon. 

   - **Environment Logic** : Iterates through FNavigationAvoidanceEdge fragments. Calculates distance from edges using LeftDir . Applies both predictive (steering) and separation (pushing) 

https://wiki.teufel-engineering.com/en/rts-unit-template 

74/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

forces based on proximity to obstacles. 

3. **Blueprint Interface** : 

   - AvoidanceStartDelay : Time in seconds before avoidance becomes active. 

4. **Component Architecture** : 

   - **Constructor** : Executes in the Avoidance group after UnitMovementProcessor and LOD . 

   - **Phase** : EMassProcessingPhase::PrePhysics . 

   - **Requirements** : Derived requirements from UMassMovingAvoidanceProcessor plus custom requirements for UMassNavigationSubsystem . 

5. **Network/Replication** : Standalone | Server | Client execution flags. 

### **UDynamicObstacleRegProcessor** 

1. **Purpose** : Dynamically registers stationary units (idle, building, repairing, or paused) as obstacles in the Mass Navigation Grid, forcing moving units to path around them. 

2. **Implementation (CPP Analysis)** : 

   - **Grid Management** : Re-initializes the UMassNavigationSubsystem obstacle grid every interval with a cell size of 100.f. 

   - **Subdivision** : For units with large radii, it generates a perimeter of smaller sub-obstacles to provide a more accurate collision silhouette for the grid search. 

   - **Nav Volume Cleanup** : Tracks spawned navigation volumes in SpawnedNavVolumes and destroys them in the subsequent frame to avoid accumulation. 

3. **Blueprint Interface** : 

   - Debug : Draws red boxes for single obstacles and orange/yellow for subdivided ones. 

   - ExecutionInterval : Frequency of grid updates. 

   - NullNavAreaClass : The area class used to mark obstacles. 

4. **Component Architecture** : 

   - **Constructor** : Runs in UE::Mass::ProcessorGroupNames::Tasks group. 

   - **Phase** : EMassProcessingPhase::PrePhysics . 

   - **Special** : bRequiresGameThreadExecution = true for safe UNavigationSystemV1 interaction. 

5. **Network/Replication** : Standard local execution on server/clients. 

### **UUnitSoftAvoidanceProcessor** 

1. **Purpose** : A corrective processor that detects units pushed outside valid navigation areas or into "dirty" obstacle zones and applies forces to push them back to the NavMesh. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

75/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Detection** : Uses ProjectPointToNavigation with ZExtent (default 5000.f) to find valid ground. It queries ARecastNavMesh to check if a unit's current polygon is marked with UNavArea_Obstacle . 

   - **Recovery Search** : If stuck in a dirty area, it performs a radial search at increasing distances (100f to 800f) to find the nearest "clean" NavMesh point. 

   - **Force** : Applies AvoidanceStrength directed towards the target valid location. 

3. **Blueprint Interface** : 

   - AvoidanceStrength : Magnitude of the corrective force. 

   - ZExtent : Vertical reach for NavMesh projection. 

4. **Component Architecture** : 

   - **Constructor** : Assigned to Avoidance group. 

   - **Phase** : EMassProcessingPhase::PrePhysics . 

   - **Tagging** : Deferentially adds/removes FMassSoftAvoidanceTag to indicate if a unit is currently undergoing recovery. 

5. **Network/Replication** : Server | Client | Standalone execution flags to maintain simulation parity across the network. 

# **Mass Projectile Module Technical Documentation UMassProjectileImpactProcessor** 

1. **Purpose** : Handles collision detection logic between Mass-based projectiles and units or the landscape. It manages damage application, piercing logic, and impact triggers. 

2. **Implementation (CPP Analysis)** : 

   - **Queries** : Defines ProjectileQuery (for active projectiles) and UnitQuery (for potential unit targets). 

   - **Optimization** : Caches unit data (locations, teams, characteristics) into local arrays before processing projectiles to avoid repeated chunk iteration. 

   - **Landscape Collision** : Checks for pre-calculated landscape impacts ( bHasLandscapeImpact ). Uses a distance squared check with a SpeedBuffer ( Speed * DeltaTime ) to prevent projectiles from passing through geometry between frames. 

   - **Unit Collision** : Performs distance checks between projectiles and units. Uses UnitCharFrags[j].GetRadiusInDirection to calculate dynamic collision bounds based 

   - on unit orientation. 

   - **Piercing Logic** : Tracks HitEntities in the FMassProjectileFragment (up to 16) to ensure single-hit-per-unit. Increments PiercedTargets and destroys the entity when MaxPiercedTargets is reached. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

76/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Damage Dispatch** : On the server ( NM_Client check), it resolves the AUnitBase actor from FMassActorFragment and calls HandleProjectileImpact directly. 

3. **Blueprint Interface** : Uses UnitSignals::ProjectileImpact to signal hits to the Mass Signal Subsystem. 

4. **Component Architecture** : Inherits from UMassProcessor . Configured for 

   - EMassProcessingPhase::PostPhysics with bRequiresGameThreadExecution = 

   - true due to direct Actor and Signal Subsystem interaction. 

5. **Network/Replication** : Authoritative on the server for damage and CDO-based GroundHit logic. Clients perform visual cleanup (scale/move ISM, destroy Niagara components). 

### **UMassRotateToMouseProcessor** 

1. **Purpose** : Synchronizes the rotation of entities with the player's mouse cursor location in the world. 

2. **Implementation (CPP Analysis)** : 

   - **Local Input** : Retrieves the local player controller ( AExtendedControllerBase ) and performs a visibility line trace under the cursor to find the CurrentMouseHit . 

   - **Server Replication** : Local clients call Server_UpdateMouseLocation to sync their target point to the server. 

   - **Orientation Logic** : Calculates the target quaternion using Dir.ToOrientationQuat() (ignoring Z-axis difference). 

   - **Interpolation** : Uses FQuat::Slerp for smooth rotation based on Characteristics[i].RotationSpeed . 

   - **Actor Sync** : If a bound Actor exists, it calls Actor->SetActorRotation to keep the visual representation in sync with the Mass fragment. 

3. **Blueprint Interface** : Reacts to UnitSignals::UpdateMouseLocation . 

4. **Component Architecture** : Inherits from UMassProcessor . Runs in PostPhysics phase. Requires game thread execution for accessing Player Controllers and Actors. 

5. **Network/Replication** : Uses AExtendedControllerBase::ReplicatedMouseLocation to drive rotation on the server and non-owning clients. 

### **UProjectileVisualManager** 

1. **Purpose** : A World Subsystem that manages the lifecycle of Mass projectiles and provides optimized Instanced Static Mesh (ISM) pooling. 

2. **Implementation (CPP Analysis)** : 

   - **ISM Pooling** : Maintains an ISMPool ( TMap<FMeshMaterialKey, UInstancedStaticMeshComponent*> ) to share ISM components across different projectile types with identical mesh/material/shadow settings. 

   - **Manager Actor** : Spawns and manages a transient ProjectileVisualISMManagerActor as a container for all pooled ISM components. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

77/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Spawning Logic** : SpawnMassProjectile handles entity creation, fragment initialization, and CDO parameter caching. It includes a FMassDeferredSetCommand wrapper to allow safe spawning during Mass processing phases. 

   - **Pre-calculation** : Performs initial line traces for EnergyWall and Landscape impacts at spawn time to optimize subsequent frame-by-frame processor checks. 

   - **VFX Management** : Spawns and attaches Niagara systems ( Niagara_A , Niagara_B ) to the manager actor's root. 

3. **Blueprint Interface** : 

   - SpawnMassProjectile : Primary API for launching mass projectiles with extensive parameter 

   - overrides (Homing, Arc, Damage, etc.). 

   - GetProjectileTransform : Utility to retrieve world transform from a Mass entity handle. 

4. **Component Architecture** : Inherits from UWorldSubsystem . 

5. **Network/Replication** : Implements client-side entity handle resolution. Since handles are not replicated, it uses UMassActorBindingComponent to find the correct ShooterEntity and TargetEntity handles locally on clients based on the provided AActor pointers. 

### **UMassProjectileMovementProcessor** 

1. **Purpose** : Simulates projectile trajectories, covering linear flight, parabolic arcs, and complex homing behaviors. 

2. **Implementation (CPP Analysis)** : 

   - **CDO Synchronization** : Periodically (every 120 frames) updates fragment variables (RotationSpeed, MaxLifeTime, etc.) from the AProjectile Class Default Object (CDO) to support live-tweaking. 

   - **Trajectory Types** : 

      - 

         - **Linear** : Standard direction-based movement. 

      - **Arc** : Uses FMath::Lerp with a parabolic height offset: 4.0 * EffectiveArcHeight * Alpha * (1.0 - Alpha) . 

      - **Homing** : Implements spiral movement using sine/cosine offsets. The HomingMaxSpiralRadius is dynamically reduced as the projectile nears the target to prevent 

      - infinite circling. 

   - **Collision Check (Wall)** : Monitors distance to pre-calculated WallImpactLocation . Triggers HandleProjectileImpact or VFX via FireEffectsAtLocation on the server when the 

   - wall is reached. 

   - **Visual Updates** : Updates ISM instance transforms and Niagara component world transforms every frame based on the entity's current FTransformFragment . 

3. **Blueprint Interface** : Internal processor; does not expose direct UFUNCTIONS. 

4. **Component Architecture** : Inherits from UMassProcessor . Phase: PostPhysics . bRequiresGameThreadExecution = true for Niagara and ISM component updates. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

78/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Ensures visual consistency on clients by forcing ISM visibility 

   - ( SetHiddenInGame(false) ) and deactivating Niagara components upon entity destruction. 

# **Mass Replication Technical Documentation** 

This document provides a deep-dive analysis of the custom Mass replication pipeline designed for the RTS Unit Template. 

### **FUnitRegistryItem** 

1. **Purpose** : A data structure representing a single entry in the authoritative unit registry, mapping network identifiers to stable game keys. 

2. **Implementation (CPP Analysis)** : Inherits from FFastArraySerializerItem . It stores a stable FName OwnerName , an int32 UnitIndex (the preferred unique key), and the associated FMassNetworkID NetID . 

3. **Blueprint Interface** : Exposes its members via UPROPERTY() . 

4. **Component Architecture** : Plain data struct intended for use within FUnitRegistryArray . 

5. **Network/Replication** : Managed by Unreal's Fast Array Serializer for efficient delta replication. 

### **FUnitRegistryArray** 

1. **Purpose** : A specialized Fast Array container for FUnitRegistryItem that handles delta serialization and provides search utilities. 

2. **Implementation (CPP Analysis)** : Inherits from FFastArraySerializer . Implements NetDeltaSerialize using FastArrayDeltaSerialize . Provides utility functions FindByOwner , FindByUnitIndex , RemoveByOwner , and RemoveByUnitIndex using TArray::FindByPredicate and TArray::RemoveAll . 

3. **Blueprint Interface** : Exposes the Items array. 

4. **Component Architecture** : Holds a raw pointer to AUnitRegistryReplicator as its owner. 

5. **Network/Replication** : Uses TStructOpsTypeTraits with WithNetDeltaSerializer = true . 

### **UUnitClientTagSyncProcessor** 

1. **Purpose** : Responsible for synchronizing Mass Tag-derived state from entities back to their corresponding AAbilityUnit actors on clients and the server. 

2. **Implementation (CPP Analysis)** : Iterates over all AAbilityUnit actors using TActorIterator . It retrieves the entity handle from the unit's UMassActorBindingComponent . It uses ComputeState (client) or ComputeStateServer (server) to check for various tags (e.g., FMassStateDeadTag , FMassStateAttackTag ) and calculates a UnitData::EState . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

79/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

It then calls ApplyStateToActor to update the unit's state. It also handles deferred signaling for casting states using UMassSignalSubsystem . 

3. **Blueprint Interface** : bShowLogs for debugging state transitions. 

4. **Component Architecture** : UMassProcessor registered with 

   - EMassProcessingPhase::PrePhysics . Requires game thread execution. 

5. **Network/Replication** : Executes on both client and server to keep actor states in sync with Mass state. 

### **AUnitClientBubbleInfo** 

1. **Purpose** : An actor that acts as the replication "bubble" container, hosting the collection of replicated Mass entity payloads for clients. 

2. **Implementation (CPP Analysis)** : Inherits from AMassClientBubbleInfoBase . In its constructor, it sets the Agents.OwnerBubble pointer and configures the net update frequency based on the net.RTS.Bubble.NetUpdateHz CVAR. It implements OnRep_Agents to handle logic when 

the agent list is updated on clients. 

3. **Blueprint Interface** : Exposes the Agents array. 

4. **Component Architecture** : Standard Unreal Actor. 

5. **Network/Replication** : bReplicates = true and bAlwaysRelevant = true . Uses FUnitReplicationArray for delta replication of unit state. 

### **URTSWorldCacheSubsystem** 

1. **Purpose** : Provides centralized caching for frequently accessed replication-related objects (registry, bubble, actor bindings) to avoid expensive lookups. 

2. **Implementation (CPP Analysis)** : Maintains TWeakObjectPtr caches for the AUnitRegistryReplicator and AUnitClientBubbleInfo . It also maintains TMap 

caches for UMassActorBindingComponent lookups by OwnerName , UnitIndex , and NetID . It includes RebuildBindingCacheIfNeeded which throttles actor iteration based on a 

configurable interval. 

3. **Blueprint Interface** : Methods like GetRegistry , GetBubble , FindBindingByUnitIndex , and FindBindingByMassNetID . 

4. **Component Architecture** : UWorldSubsystem . 

5. **Network/Replication** : Non-replicated, purely local performance optimization. 

### **UMassUnitReplicatorBase** 

1. **Purpose** : The server-side logic that serializes Mass entity fragments and tags into the FUnitReplicationItem payloads within the bubble. 

2. **Implementation (CPP Analysis)** : 

   - AddEntity : Pre-populates the replication item with stable data (classes, offsets) when an entity is 

   - first registered. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

80/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - ProcessClientReplication : Iterates over entities, builds the TagBits bitfield, and 

   - populates fields from fragments like FTransformFragment , FMassAITargetFragment , FMassCombatStatsFragment , etc. It uses thresholds (controlled by CVARs) to determine if an 

   - item is dirty and needs replication. 

3. **Blueprint Interface** : Inherits from UMassReplicatorBase . 

4. **Component Architecture** : Managed as a replicator within the Mass Replication framework. 

5. **Network/Replication** : Server-only logic that drives the population of the replicated Agents array. 

### **UServerReplicationKickProcessor** 

1. **Purpose** : A server-only processor that ensures the replication pipeline is "kicked" (executed) for entities, even if Mass doesn't consider them dirty, and manages the match startup freeze. 

2. **Implementation (CPP Analysis)** : 

   - Handles the release of the FMassStateFrozenTag when MatchStartTime is reached. 

   - Implements a custom slice-based budget for replication processing using CVARs like net.RTS.ServerKick.MaxPerTick . 

   - It computes a lightweight signature ( FSig ) for entities (Location, Rotation, Tags, Health, etc.) and compares it against GLastSigByID . If the signature changes, it invokes the replicator for that slice. 

3. **Blueprint Interface** : Governed by multiple console variables for tuning performance and logging. 

4. **Component Architecture** : UMassProcessor running in PrePhysics . Uses FWorldDelegates::OnWorldCleanup to manage its static signature cache. 

5. **Network/Replication** : Server-only "driver" for the custom replication pipeline. 

### **AUnitRegistryReplicator** 

1. **Purpose** : The authoritative source of truth on the server for mapping Mass entities to Units via NetIDs. 

2. **Implementation (CPP Analysis)** : 

   - Manages a monotonic NextNetID counter. 

   - QuarantineNetID : Implements a quarantine period for destroyed IDs to prevent rapid reuse. 

   - ServerDiagnosticsTick : Periodically reconciles the registry with live actors in the world to find 

   - unregistered units or prune stale entries. 

3. **Blueprint Interface** : AreAllUnitsRegistered , GetRegistrationProgress , GetRegistrationCounts . 

4. **Component Architecture** : A replicated Actor. 

5. **Network/Replication** : bReplicates = true and bAlwaysRelevant = true . Replicates the FUnitRegistryArray to all clients. 

### **FUnitReplicationItem** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

81/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : The core data structure for replicated unit state, containing transforms, combat stats, AI state, and packed tags. 

2. **Implementation (CPP Analysis)** : 

   - Uses FVector_NetQuantize for locations. 

   - Quantizes rotation into uint16 values ( PitchQuantized etc.). 

   - PostReplicatedAdd / PostReplicatedChange : On clients, these callbacks update the UnitReplicationCache and handle projectile spawning by comparing the replicated AIS_ProjectileFireCounter . 

3. **Blueprint Interface** : Large set of UPROPERTY() fields covering fragments like FMassCombatStatsFragment , FMassAgentCharacteristicsFragment , FMassAIStateFragment , and FMassMoveTargetFragment . 

4. **Component Architecture** : FFastArraySerializerItem . 

5. **Network/Replication** : Optimized for bandwidth while providing a full state snapshot for client-side representation. 

### **FUnitReplicationArray** 

1. **Purpose** : Fast array container for FUnitReplicationItem . 

2. **Implementation (CPP Analysis)** : Standard FFastArraySerializer implementation. Provides FindItemByNetID and RemoveItemByNetID . 

3. **Blueprint Interface** : Exposes the Items array. 

4. **Component Architecture** : Container struct referencing AUnitClientBubbleInfo . 

5. **Network/Replication** : Implements NetDeltaSerialize . 

### **FPendingLinkItem** 

1. **Purpose** : Tracking structure for entities awaiting linking between an actor and a Mass entity. 

2. **Implementation (CPP Analysis)** : Stores OwnerName and NetID . 

3. **Blueprint Interface** : UPROPERTY() members. 

4. **Component Architecture** : FFastArraySerializerItem . 

5. **Network/Replication** : Part of FPendingLinkArray . 

### **FPendingLinkArray** 

1. **Purpose** : Container for pending link items. 

2. **Implementation (CPP Analysis)** : FFastArraySerializer with a Contains utility. 

3. **Blueprint Interface** : Items array. 

4. **Component Architecture** : Container struct. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

82/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Implements NetDeltaSerialize . 

### **UClientReplicationProcessor** 

1. **Purpose** : The client-side consumer of replicated data, responsible for linking actors to entities and applying replicated state (transforms, stats, etc.). 

2. **Implementation (CPP Analysis)** : 

   - **Reconciliation** : Compares local entities with the authoritative registry and bubble. It triggers RequestClientMassLink for missing entities and RequestClientMassUnlink for 

   - stale ones, subject to a per-tick budget. 

   - **Transform Application** : Can perform direct snapping ( bUseFullReplication ) or gentle reconciliation. 

   - **Reconciliation Logic** : Calculates PosError and applies corrective forces to FMassForceFragment using a proportional gain Kp . Handles rotation reconciliation using KpRot . 

   - **State Application** : Syncs replicated tags, AI targets, and various fragment data directly from the bubble payload. 

3. **Blueprint Interface** : Parameters for tuning reconciliation like Kp , MaxCorrectionAccel , KpRot , and FullReplicationDistance . 

4. **Component Architecture** : UMassProcessor restricted to the client phase. 

5. **Network/Replication** : The primary client-side entry point for the custom replication system. 

# **Mass Signals Technical Deep-Dive** 

### **UUnitPresenceSignalingProcessor** 

1. **Purpose** : Throttled broadcasting of unit presence via UMassSignalSubsystem to allow detectors to find units without querying every entity every frame. 

2. **Implementation (CPP Analysis)** : 

   - Executes in EMassProcessingPhase::PrePhysics . 

   - Throttling: Execute calculates TimeSinceLastRun against ExecutionInterval . 

   - Query: EntityQuery requires FTransformFragment , FMassCombatStatsFragment , FMassAgentCharacteristicsFragment , FMassAIStateFragment , and FMassSightFragment . 

   - Logic: Iterates through chunks, collects all valid FMassEntityHandle s into AllUnits , and calls SignalSubsystem->SignalEntities with UnitSignals::UnitInDetectionRange . 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

83/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - ExecutionInterval (float, BlueprintReadWrite, EditAnywhere): Controls frequency of signal 

   - broadcasts. 

4. **Component Architecture** : 

   - Inherits from UMassProcessor . 

   - Constructor sets ProcessingPhase to PrePhysics and bAutoRegisterWithProcessingPhases = true . 

5. **Network/Replication** : 

   - Execution is local to the world simulation; typically used on the server to drive authoritative AI detection. 

### **UMassUnitSpawnerSubsystem** 

1. **Purpose** : Acts as a bridge between the Unreal Actor system and the Mass simulation by buffering AUnitBase actors that are pending entity creation. 

2. **Implementation (CPP Analysis)** : 

   - RegisterUnitForMassCreation : Adds an AUnitBase pointer to the PendingUnits 

   - array. 

   - GetAndClearPendingUnits : Iterates PendingUnits , validates pointers via UnitPtr.Get() , populates the output array, and calls Empty() on the internal buffer. 

3. **Blueprint Interface** : 

   - Public API: RegisterUnitForMassCreation , GetAndClearPendingUnits , ResetSystem . 

4. **Component Architecture** : 

   - Inherits from UWorldSubsystem . 

5. **Network/Replication** : 

   - Non-replicated world subsystem; manages local actor pointers during the transition to Mass. 

### **UUnitSignalingProcessor** 

1. **Purpose** : Orchestrates the linking of spawned AUnitBase actors to their corresponding Mass entities and manages client-side binding reconciliation. 

2. **Implementation (CPP Analysis)** : 

   - Linking: Execute retrieves pending units from UMassUnitSpawnerSubsystem and adds them to PendingRetryQueue . 

   - Deferred Execution: CreatePendingEntities is bound to the OnProcessingPhaseFinished delegate. It processes the retry queue using a CVAR-controlled 

   - budget ( net.RTS.UnitSignaling.MaxRegistrationsPerFrame ) to avoid hitches. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

84/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

- Client Reconciliation: In Execute , if bIsClient and replication mode is Mass , it uses URTSWorldCacheSubsystem to find bindings by UnitIndex or OwnerName and calls RequestClientMassLink . 

#### 3. **Blueprint Interface** : 

- ExecutionInterval : Cadence for the processor's execute loop. 

- bDebugLogs : Enables verbose logging of the linking process. 

- MaxRegistrationsPerFrame : Budget for entity creation. 

#### 4. **Component Architecture** : 

- Inherits from UMassProcessor . 

- bRequiresGameThreadExecution = true and ExecutionFlags = 

- EProcessorExecutionFlags::All . 

#### 5. **Network/Replication** : 

- Essential for high-performance replication. Supports "visual freeze" and delayed linking ( net.RTS.UnitSignaling.CreationStartDelay ) to ensure replication data is ready before binding. 

### **UUnitStateProcessor** 

1. **Purpose** : The primary bridge for synchronizing logic and state between Mass fragments and Unreal Actors, and handling signal-driven state transitions. 

2. **Implementation (CPP Analysis)** : 

   - Signal Handling: InitializeInternal binds StateChangeSignals (Idle, Chase, Attack, etc.) to ChangeUnitState . 

   - Thread Safety: Uses AsyncTask(ENamedThreads::GameThread, ...) for all operations that modify or access AUnitBase actors or the Navigation System. 

   - Attribute Sync: SynchronizeStatsFromActorToFragment updates fragments like FMassCombatStatsFragment from the actor's UAttributeSetBase . 

   - State Transitions: SwitchState handles the addition and removal of Mass tags (e.g., FMassStateIdleTag , FMassStateChaseTag ) and updates the UnitBase state. 

   - Path Following: UpdateUnitArrayMovement processes FMassUnitPathFragment to drive FMassMoveTargetFragment towards queued waypoints. 

3. **Blueprint Interface** : 

   - Debug : Toggles technical logs. 

   - BuildingSpawnTrace : Vector for ground alignment during spawning. 

   - SpawnSingleUnit : Comprehensive actor spawning with Mass configuration. 

   - SpawnWorkResource : Manages actor-to-actor attachment for resources. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

85/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

#### 4. **Component Architecture** : 

- 

      - Inherits from UMassProcessor . 

   - Manages a vast array of FDelegateHandle s for signal unbinding during BeginDestroy . 

5. **Network/Replication** : 

   - Authoritative on server for attribute sync and state machine logic. Dispatches visual updates via Actor RPCs (e.g., Multicast_RegisterBuildingAsObstacle ). 

# **Mass Building States Technical Documentation** 

### **UBuildingIdleStateProcessor** 

#### 1. **Purpose** : 

The core responsibility of this processor is to manage the logic for building-type entities when they are in an "Idle" state. It acts as a behavior controller within the Mass Framework to evaluate idle conditions and potentially trigger state transitions or signals. 

2. **Implementation (CPP Analysis)** : 

   - **Query Configuration** : ConfigureQueries initializes an FMassEntityQuery that filters for entities with the FMassStateRunTag . It requires ReadOnly access to FTransformFragment and ReadWrite access to FMassMoveTargetFragment . It 

   - explicitly excludes entities with FMassStateDeadTag or FMassIsEffectAreaTag . 

   - **Initialization** : InitializeInternal caches the UMassSignalSubsystem from the world to facilitate signal-based communication between entities and systems. 

   - 

      - **Execution Logic** : 

      - ExecutionOrder.ExecuteInGroup : Set to UE::Mass::ProcessorGroupNames::Behavior . 

      - ProcessingPhase : Set to EMassProcessingPhase::PostPhysics . 

      - Execute : Currently an empty implementation stub intended for per-tick logic. 

   - **Timers** : Uses a TimeSinceLastRun float and a configurable ExecutionInterval to throttle processing frequency if logic were implemented in Execute . 

3. **Blueprint Interface** : 

   - ExecutionInterval : UPROPERTY(BlueprintReadWrite, EditAnywhere) - 

   - Allows designers to tune the tick rate of the processor (default 0.1s). 

4. **Component Architecture** : 

   - **Constructor** : Initializes EntityQuery and sets up the execution group ( Behavior ) and processing phase ( PostPhysics ). 

   - **Subsystems** : Directly interacts with UMassSignalSubsystem for signal processing. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

86/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

#### 5. **Network/Replication** : 

- This processor runs on the server (or authoritative client in peer-to-peer). Replication of state is handled by the Mass Framework's fragment replication settings; this class itself does not implement custom RPCs or replication logic. 

### **UBuildingChaseStateProcessor** 

1. **Purpose** : 

Manages the "Chase" state logic for building-type entities. This typically involves logic where a buildingassociated entity needs to track or "chase" a target, or process proximity-based logic while in a pursuit mode. 

2. **Implementation (CPP Analysis)** : 

   - **Query Configuration** : Identical to the Idle processor, it filters for FMassStateRunTag and excludes FMassStateDeadTag and FMassIsEffectAreaTag . It requests FTransformFragment (ReadOnly) for position data and FMassMoveTargetFragment 

   - (ReadWrite) to potentially modify movement objectives. 

   - **Initialization** : Caches UMassSignalSubsystem in InitializeInternal . 

   - 

- **Execution Logic** : 

- ExecutionOrder.ExecuteInGroup : 

UE::Mass::ProcessorGroupNames::Behavior . 

- ProcessingPhase : EMassProcessingPhase::PostPhysics . 

- 

      - Execute : Currently an empty implementation stub. 

   - **Scheduling** : Inherits UMassProcessor behavior, intended to run according to the ProcessingPhase settings. 

3. **Blueprint Interface** : 

   - ExecutionInterval : UPROPERTY(BlueprintReadWrite, EditAnywhere) - 

   - Configurable float (default 0.1s) for controlling execution frequency. 

4. **Component Architecture** : 

   - **Constructor** : Sets ProcessingPhase to PostPhysics and bAutoRegisterWithProcessingPhases to true, ensuring the processor is integrated into 

   - the Mass processing pipeline automatically. 

   - **Query Mechanism** : Uses FMassEntityQuery to perform efficient bulk operations on matching entities. 

5. **Network/Replication** : 

   - Standard Mass Framework behavior. The processor operates on the local entity collection. If movement targets or state tags are replicated, the results of this processor's execution will be synchronized via the fragment replication system. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

87/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

# **Mass States Technical Documentation** 

### **UChaseStateProcessor** 

1. **Purpose** : Manages the "Chase" state, where an entity actively pursues a target within the Mass framework. 

2. **Implementation (CPP Analysis)** : 

   - ExecuteServer : Authoritative logic using UpdateMoveTarget to set FMassMoveTargetFragment toward the target's last known location. It incorporates complex 

   - distance checks factoring in both attacker and target capsule/box radii via 

      - GetRadiusInDirection . 

   - ExecuteClient : Performs local tag manipulation for responsiveness. If HoldPosition is 

   - toggled or a target is lost, it locally swaps tags to FMassStateIdleTag . 

   - CalculateChaseOffset : A deterministic utility using the Golden Angle (137.5<sup>∘</sup> ) and SplitMix64- 

   - style scrambling to provide unique pursuit offsets per entity. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : Inherits from UMassProcessor . Configured for EMassProcessingPhase::PostPhysics within the Behavior group. 

5. **Network/Replication** : Server-side authoritative movement; client-side local tag prediction for state transitions. 

### **UPauseStateProcessor** 

1. **Purpose** : Represents an "inter-action" delay, typically used between a chase and an attack or as a cooldown between individual attacks. 

2. **Implementation (CPP Analysis)** : 

   - ServerExecute : Monitors StateTimer against FMassCombatStatsFragment::PauseDuration . Performs range checks similar to Chase. 

   - Triggers Attack or RangedAttack signals via SignalEntityDeferred when conditions are met. 

   - ClientExecute : Implements client-side prediction for projectiles. It calculates target range and 

   - spawns visual-only projectiles via UProjectileVisualManager using PredictionTimer to mask latency. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor child. Operates in PostPhysics phase, Behavior group. 

5. **Network/Replication** : Uses EProcessorExecutionFlags::All . Server manages state; client manages predictive visual effects. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

88/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **UDeathStateProcessor** 

1. **Purpose** : Handles the cleanup and lifecycle termination of dead Mass entities. 

2. **Implementation (CPP Analysis)** : 

   - Registers for RemoveDeadUnit and HideUnit signals. 

   - HandleRemoveDeadUnit : Dispatched to AsyncTask(ENamedThreads::GameThread) to safely interact with AUnitBase actors, 

   - deselecting them and updating the HUD's SelectedUnits array. 

   - ExecuteServer : Forces velocity to zero, increments death timers, and signals EndDead for 

   - final entity destruction after DespawnTime . 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor . Requires FMassActorFragment for GameThread actor access. 

5. **Network/Replication** : Server drives the destruction lifecycle; Client handles local actor hiding via UUnitVisualManager . 

### **UAttackStateProcessor** 

1. **Purpose** : Executes the "Melee" or "Ranged Impact" phase of combat. 

2. **Implementation (CPP Analysis)** : 

   - Execute : Checks if the target is still alive/valid. Increments StateTimer . 

   - For melee units, if StateTimer <= AttackDuration , it triggers the MeleeAttack signal exactly once per cycle using StateFrag.HasAttacked latch. 

   - Transitions entities to the Pause state upon completion of the attack duration. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor . Operates in PostPhysics / Behavior . 

5. **Network/Replication** : Marked Server | Standalone . Combat impact logic is server-authoritative. 

### **UPatrolRandomStateProcessor** 

1. **Purpose** : Governs movement toward random waypoints within a designated patrol area. 

2. **Implementation (CPP Analysis)** : 

   - Execute : Monitors distance to the current MoveTarget.Center . 

   - Upon reaching the destination (defined by AcceptanceRadius * 4 ), it clears movement via StopMovement and transitions the entity to PatrolIdle . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

89/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ Constantly checks for valid targets to pivot into the Chase state. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor . Uses FMassPatrolFragment . 

5. **Network/Replication** : Server-side authoritative logic. 

### **UIdleStateProcessor** 

1. **Purpose** : The default rest state for entities, managing target scanning and administrative behaviors. 

2. **Implementation (CPP Analysis)** : 

   - Implements "Friendly Follow" logic: If a friendly target is assigned, it calculates a ring position at FollowRadius using deterministic angular distribution. 

   - Handles HoldPosition : Allows entities to transition to Pause (to attack) only if enemies enter range, but prevents chasing. 

   - Manages automatic patrol reversion via SetUnitsBackToPatrolTime . 

3. **Blueprint Interface** : 

   - 

      - ExecutionInterval : Update frequency. 

   - bSetUnitsBackToPatrol , SetUnitsBackToPatrolTime : Configuration for automatic 

   - state reversion. 

4. **Component Architecture** : UMassProcessor . Uses FMassUnitPathFragment to determine if it should ignore enemies while pathing. 

5. **Network/Replication** : Server-side authoritative. 

### **URunStateProcessor** 

1. **Purpose** : The primary movement processor for non-combat travel. 

2. **Implementation (CPP Analysis)** : 

   - ExecuteServer : Handles complex "Follow" movement, including UNavigationSystemV1::ProjectPointToNavigation and obstacle avoidance. If 

   - following a building, it uses LastGroundLocation to stabilize Z-height. 

   - ExecuteClient : Detects arrival at the MoveTarget locally and performs a bulk tag 

   - removal/addition to switch to Idle instantly for the local player. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Update frequency. 

   - bShowLogs : Debug logging toggle. 

4. **Component Architecture** : UMassProcessor . Integrates with FMassVelocityFragment . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

90/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Explicit split between ExecuteClient and ExecuteServer . Movement is replicated via Mass bubbles, but state transitions are predicted on clients. 

### **UIsAttackedStateProcessor** 

1. **Purpose** : Handles a brief "stagger" or "reaction" state when an entity is damaged. 

2. **Implementation (CPP Analysis)** : 

   - Execute : Increments StateTimer against IsAttackedDuration . 

   - Once the duration expires, it prioritizes transitioning to Chase if a target is available, otherwise it signals SetUnitStatePlaceholder to resume previous activity. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor . Requires FMassCombatStatsFragment . 

5. **Network/Replication** : Server-side authoritative. 

### **UPostBindingInitProcessor** 

1. **Purpose** : A hook for logic that must execute once an actor is bound to a Mass entity. 

2. **Implementation (CPP Analysis)** : Currently serves as a container for future initialization logic. Requires FMassActorFragment . 

3. **Blueprint Interface** : ExecutionInterval . 

4. **Component Architecture** : UMassProcessor . Configured for EMassProcessingPhase::PostPhysics in the Tasks group. 

5. **Network/Replication** : Standard processor flags. 

### **UPatrolIdleStateProcessor** 

1. **Purpose** : Manages the stationary period at a patrol waypoint. 

2. **Implementation (CPP Analysis)** : 

   - Execute : Forces Velocity.Value to zero. 

   - Generates a random IdleDuration per entity. After the timer expires, it performs a probability roll against PatrolFrag.IdleChance to decide whether to trigger PISwitcher (moving to the next waypoint). 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.5s). 

4. **Component Architecture** : UMassProcessor . Uses FMassPatrolFragment . 

5. **Network/Replication** : Server-side authoritative. 

**UCastingStateProcessor** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

91/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Manages the state and timing for ability execution. 

2. **Implementation (CPP Analysis)** : 

   - ExecuteServer : Increments cast timers and signals SyncCastTime . Triggers EndCast 

   - upon completion. Sets bRotateTowardsAbility on the target fragment. 

   - ExecuteClient : Mirrors timer logic and rotation flags. 

   - HandleClientSetToPlaceholder : An AsyncTask on the GameThread that performs a 

   - full state transition on the client, updating both Mass tags and the AUnitBase actor state to ensure visual synchronization. 

3. **Blueprint Interface** : 

   - ExecutionInterval : Throttles logic updates (Default 0.1s). 

4. **Component Architecture** : UMassProcessor . Requires FMassAIStateFragment and FMassCombatStatsFragment . 

5. **Network/Replication** : Uses SignalEntityDeferred for server-to-client sync of cast progress. Client handles local actor state via signal delegates. 

### **URunAnimationProcessor** 

1. **Purpose** : A utility processor for managing temporary tags used for animations or timed effects. 

2. **Implementation (CPP Analysis)** : 

   - Execute : Scans for FRunAnimationTag . Updates StateTimer against FRunAnimationFragment::Duration . 

   - Uses Context.Defer() to remove both the tag and the fragment once the duration is reached. 

3. **Blueprint Interface** : None. 

4. **Component Architecture** : UMassProcessor . Lightweight, logic-only processor. 

5. **Network/Replication** : Executes on all instances to keep tags synced. 

### **UMainStateProcessor** 

1. **Purpose** : The "God" processor for unit lifecycle, health monitoring, and global synchronization. 

2. **Implementation (CPP Analysis)** : 

   - ExecuteServer : Authoritatively handles health dropping below zero, signaling the Dead state. 

   - Manages the reversion of LoseSightRadius if it was temporarily extended. Triggers SyncUnitBase and UnitSpawned signals. 

   - ExecuteClient : Monitors FMassCombatStatsFragment health. If <= 0, it bulk-removes 

   - all state tags and adds FMassStateDeadTag locally. 

   - HandleUpdateSelectionCircle : Triggers GameThread UI updates for unit selection. 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

92/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - ExecutionInterval : Frequency of health/state checks. 

   - UpdateCircleInterval : Frequency of UI circle updates. 

4. **Component Architecture** : UMassProcessor . Central hub for state-wide signals. 

5. **Network/Replication** : Distinguishes between server-authoritative death and client-side visual state cleanup. 

# **Mass Worker States Technical Documentation** 

Technical deep-dive into the Mass Processor implementations for worker state transitions and logic. 

### **UGoToResourceExtractionStateProcessor** 

1. **Purpose** : Manages the movement of units towards a resource node for extraction. 

2. **Implementation (CPP Analysis)** : 

   - Queries for FMassStateGoToResourceExtractionTag . 

   - Calculates distance to WorkerStatsFrag.ResourcePosition . 

   - If DistanceToTargetCenter <= WorkerStatsFrag.ResourceArrivalDistance + 50.f , it sets AIState.SwitchingState = true , calls StopMovement , and signals UnitSignals::ResourceExtraction . 

   - Handles redirection to UnitSignals::GoToBuild if a building area becomes available. 

3. **Blueprint Interface** : ExecutionInterval (float) - frequency of execution. 

4. **Component Architecture** : Configured for Server | Standalone , Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server-side execution only. 

### **UResourceExtractionStateProcessor** 

1. **Purpose** : Manages the resource extraction process once the unit has arrived at the resource. 

2. **Implementation (CPP Analysis)** : 

   - **Server** : Increments StateTimer . If StateTimer >= WorkerStatsFrag.ResourceExtractionTime , it signals UnitSignals::GetResource and UnitSignals::UpdateResourceScale . 

   - **Client** : If Vis.bIsOnViewport , signals UnitSignals::ResourceExtraction . Uses HandleUpdateResourceScale (AsyncTask on GameThread) to visually shrink the resource 

   - actor. 

3. **Blueprint Interface** : ExecutionInterval (float). 

https://wiki.teufel-engineering.com/en/rts-unit-template 

93/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Configured for Server | Standalone | Client , Behavior group, PostPhysics phase. 

5. **Network/Replication** : Synchronized execution on server and client for visual scaling. 

### **UGoToRepairStateProcessor** 

1. **Purpose** : Navigates units to a friendly target that requires repairs. 

2. **Implementation (CPP Analysis)** : 

   - Calculates EffectiveReach using AttackerRadius + TargetRadius + FollowRadius . 

   - Uses CharFrag.GetRadiusInDirection for dynamic radius calculation based on movement direction. 

   - If Dist2D <= (EffectiveReach - 20.f) , it stops movement and signals UnitSignals::Repair . 

   - Otherwise, it updates move target to a DesiredPos on the FollowRadius ring. 

3. **Blueprint Interface** : ExecutionInterval (float). 

4. **Component Architecture** : Configured for Server | Standalone , Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server-side execution only. 

### **UGoToBaseStateProcessor** 

1. **Purpose** : Guides units back to their base or drop-off point. 

2. **Implementation (CPP Analysis)** : 

   - **Server** : Checks distance to WorkerStats.BasePosition . If within BaseArrivalDistance , signals UnitSignals::ReachedBase . 

   - **Client** : If the base is reached or unavailable, it performs immediate local state cleanup by removing multiple tags and adding FMassStateIdleTag . 

3. **Blueprint Interface** : ExecutionInterval (float). 

4. **Component Architecture** : Configured for Server | Standalone | Client , Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server authoritative with client-side prediction/cleanup. 

### **UBuildStateProcessor** 

1. **Purpose** : Manages the active building construction state. 

2. **Implementation (CPP Analysis)** : 

   - **Server** : Increments StateTimer . If StateTimer >= WorkerStats.BuildTime , it signals UnitSignals::SpawnBuildingRequest . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

94/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - Updates unit rotation to face WorkerStats.BuildAreaPosition . 

   - Signals UnitSignals::SyncCastTime every execution tick. 

3. **Blueprint Interface** : ExecutionInterval (float). 

4. **Component Architecture** : Configured for All execution flags, Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server authoritative construction logic. 

### **UGoToBuildStateProcessor** 

1. **Purpose** : Moves units to a designated building area to begin construction. 

2. **Implementation (CPP Analysis)** : 

   - Checks distance to WorkerStats.BuildAreaPosition . 

   - If DistanceToTargetCenter <= WorkerStats.BuildAreaArrivalDistance , it stops movement and signals UnitSignals::Build . 

   - Validates site availability and redirects to base if the build area is no longer valid. 

3. **Blueprint Interface** : ExecutionInterval (float). 

4. **Component Architecture** : Configured for Server | Standalone , Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server-side execution only. 

### **URepairStateProcessor** 

1. **Purpose** : Manages the active repairing of a friendly target. 

2. **Implementation (CPP Analysis)** : 

   - **Server** : Validates target health and distance (uses a 40-unit ExitBuffer ). 

   - If out of range, signals UnitSignals::GoToRepair . 

   - Updates unit rotation to face the target. 

   - When StateTimer >= StatsFrag.CastTime , signals UnitSignals::GoToBase . 

   - Signals UnitSignals::SyncRepairTime for progress bars. 

3. **Blueprint Interface** : ExecutionInterval (float). 

4. **Component Architecture** : Configured for All execution flags, Behavior group, PostPhysics phase. 

5. **Network/Replication** : Server authoritative repair completion. 

# **Mass Module Technical Documentation** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

95/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

This document provides a deep-dive technical analysis of the classes within the Mass module of the RTS Unit Template. 

### **UUnitVisibilityProcessor** 

1. **Purpose** : Manages entity visibility states, viewport detection, and UI element (healthbar) visibility logic. 

2. **Implementation (CPP Analysis)** : Throttled execution via TimeSinceLastRun and ExecutionInterval (default 0.05s). Uses 

   - UGameplayStatics::ProjectWorldToScreen for viewport checks. Logic evaluates ConsistentTeamOverlapsPerTeam and 

ConsistentAttackerTeamOverlapsPerTeam from FMassSightFragment to determine visibility against the local player's team. Dispatches signals via SignalSubsystem>SignalEntities . 

3. **Blueprint Interface** : DefaultHealthbarVisibleTime (float), PositiveChangeThreshold (float), and HandleVisibilitySignals (UFUNCTION). 

4. **Component Architecture** : Inherits from UMassProcessor . Configures EntityQuery with requirements for FTransformFragment , FMassCombatStatsFragment , FMassVisibilityFragment , FMassActorFragment , FMassAgentCharacteristicsFragment , and FMassSightFragment . 

5. **Network/Replication** : Runs on Client, Standalone, and Server. Server-side logic ensures visibility flags are defaulted to true for processing consistency. 

### **UUnitRotateToTargetProcessor** 

1. **Purpose** : Handles smooth rotation of units toward their AI targets or specific focus points. 

2. **Implementation (CPP Analysis)** : Calculates target rotation using FQuat::Slerp based on delta time and FMassUnitYawFollowFragment::Duration . Resolves target location from 

   - FMassAITargetFragment . Updates 

   - FMassAgentCharacteristicsFragment::PositionedTransform and sets bTransformDirty . 

3. **Blueprint Interface** : Uses FMassUnitYawFollowFragment and FMassUnitYawFollowTag . 

4. **Component Architecture** : Inherits from UMassProcessor . Executes in PostPhysics phase. Explicitly ordered to run before ActorTransformSyncProcessor . 

5. **Network/Replication** : Executes on Client, Server, and Standalone. 

### **UMassActorBindingComponent** 

1. **Purpose** : Authoritative bridge for binding traditional Actors to Mass Entities, managing fragment initialization and replication registration. 

2. **Implementation (CPP Analysis)** : Manages lifecycle via CreateAndLinkOwnerToMassEntity and CleanupMassEntity . Synchronously initializes fragments: InitTransform , 

https://wiki.teufel-engineering.com/en/rts-unit-template 

96/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

InitMovementFragments , InitAIFragments , InitRepresentation , and InitStats . Server-side logic assigns FMassNetworkID via 

AUnitRegistryReplicator . 

3. **Blueprint Interface** : BindingType (EMassBindingType), SetupMassOnActor (UFUNCTION), RequestClientMassLink (UFUNCTION), and various tuning parameters (SightRadius, 

MaxAcceleration, etc.). 

4. **Component Architecture** : USceneComponent specialization. Implements FMassArchetypeSharedFragmentValues for batching movement and avoidance parameters. 

5. **Network/Replication** : Server drives entity creation and registry assignment. Client uses IsReadyForClientMassLink to wait for authoritative data (NetID and Bubble sync) before local 

binding. 

### **ULookAtProcessor** 

1. **Purpose** : Calculates "LookAt" rotations for units in Attack or Pause states, updating their visual facing. 

2. **Implementation (CPP Analysis)** : (Analysis based on available header and logic structure) Calculates orientation toward targets in XY plane. Uses LineTrace for ground height determination. Dispatches updates via FActorTransformUpdatePayload to the Game Thread. 

3. **Blueprint Interface** : AccumulatedTimeA (float). 

4. **Component Architecture** : Inherits from UMassProcessor . PrePhysics phase. 

5. **Network/Replication** : Local visual processing based on replicated target and transform data. 

### **UUnitApplyMassMovementProcessor** 

1. **Purpose** : Integrates forces and steering into final velocity and location updates, handling specialized movement modes. 

2. **Implementation (CPP Analysis)** : Distinct ExecuteServer and ExecuteClient paths. Clamps velocity based on FMassMovementParameters . Implements "Soft Avoidance" by projecting to navmesh and checking for UNavArea_Obstacle (Energy Walls). Handles horizontal movement freezing via FMassStateStopXYMovementTag . 

3. **Blueprint Interface** : bShowLogs (bool), SoftAvoidanceZExtent (float). 

4. **Component Architecture** : Inherits from UMassProcessor . PrePhysics phase, ordered after Avoidance group. 

5. **Network/Replication** : Synchronized via authoritative fragment updates; client performs local integration for smoothness. 

### **UUnitSightProcessor** 

1. **Purpose** : Authoritative vision system, detection of invisible entities, and local fog-of-war mask management. 

2. **Implementation (CPP Analysis)** : Throttled update (0.2s). Iterates over all entities to populate TeamOverlapsPerTeam and DetectorOverlapsPerTeam based on squared distance 

https://wiki.teufel-engineering.com/en/rts-unit-template 

97/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

checks. Dispatches UnitSignals::UpdateFogMask signals. Uses 

AsyncTask(ENamedThreads::GameThread) to update local fog/minimap. 

3. **Blueprint Interface** : HandleSightSignals and HandleUpdateFogMask (UFUNCTIONs). 

4. **Component Architecture** : Inherits from UMassProcessor . PostPhysics phase. Configures EntityQuery and EffectAreaQuery . 

5. **Network/Replication** : Server-side performs authoritative detection. Client-side handles local fog visualization. 

### **UMassUnitVisualTweenProcessor** 

1. **Purpose** : Procedural animation system for ISM instances, providing tweens and periodic visual effects. 

2. **Implementation (CPP Analysis)** : Updates tween states (Rotation, Location, Scale) using FMath::QInterpConstantTo or FQuat::Slerp . Implements periodic logic: Pulsate 

(Sine/Cosine scale), Continuous Rotation (Axis/Speed), and Oscillation (Offset A/B). Features "Yaw-toChase" for specific ISM parts. Sets CharList[i].bTransformDirty . 

3. **Blueprint Interface** : bLogDebug (bool). 

4. **Component Architecture** : Inherits from UMassProcessor . PrePhysics phase. Requires Game Thread execution for ISM component access. 

5. **Network/Replication** : Local-only visual updates driven by replicated state/target fragments. 

### **UMassResourcePlacementProcessor** 

1. **Purpose** : Places carried resource ISMs relative to worker units, typically attached to a specific mesh socket. 

2. **Implementation (CPP Analysis)** : Locates ResourceSocket on skeletal meshes. Applies SocketOffset and ResourceScale . Batches updates using ISM- 

>BatchUpdateInstancesTransforms for performance. Handles visibility via a hidden transform. 

3. **Blueprint Interface** : None. 

4. **Component Architecture** : Inherits from UMassProcessor . PostPhysics phase, ordered after ActorTransformSyncProcessor . 

5. **Network/Replication** : Client-side visual placement. 

### **UMassUnitPlacementProcessor** 

1. **Purpose** : Final synchronization of Mass entity transforms to the Instanced Static Mesh (ISM) rendering system. 

2. **Implementation (CPP Analysis)** : Implements LOD-based culling (LOD::Off hides instances). Uses CharList[i].bTransformDirty to skip redundant UpdateInstanceTransform calls. 

Sorts batched updates by InstanceIndex for cache efficiency. Calls ISM>MarkRenderDynamicDataDirty for motion vector support. 

3. **Blueprint Interface** : None. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

98/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Inherits from UMassProcessor . PostPhysics phase, ordered after ActorTransformSyncProcessor . 

5. **Network/Replication** : Visual sync on all platforms. 

### **UCustomMassModuleSettings** 

1. **Purpose** : Global configuration storage for the Mass module's customizable parameters. 

2. **Implementation (CPP Analysis)** : Standard specialization of UMassModuleSettings . 

3. **Blueprint Interface** : Exposed via the project's Mass settings menu. 

4. **Component Architecture** : Data-driven settings class. 

5. **Network/Replication** : Static configuration. 

### **UUnitMovementProcessor** 

1. **Purpose** : Core pathfinding logic and steering intent for Mass entities. 

2. **Implementation (CPP Analysis)** : Integrates UNavigationSystemV1 . RequestPathfindingAsync utilizes background tasks to perform FindPathSync . 

Implements "Strict Mode" filters for UNavArea_EnergyWall . Features "Escape Mode" to handle units stuck inside obstacles by allowing partial paths. Handles flight differently (direct 3D steering). 

3. **Blueprint Interface** : NavMeshProjectionExtent (FVector), ExecutionInterval (float). 

4. **Component Architecture** : Inherits from UMassProcessor . PrePhysics phase, Tasks group. 

5. **Network/Replication** : Server-authoritative pathfinding; client uses FMassClientPredictionFragment for low-latency starts. 

### **UActorTransformSyncProcessor** 

1. **Purpose** : Bi-directional synchronization between Mass entity fragments and Game Thread Actors, including ground alignment. 

2. **Implementation (CPP Analysis)** : Implements dynamic tick rates based on FPS thresholds 

   - ( MinTickInterval to MaxTickInterval ). HandleGroundAndHeight performs LineTraces to determine ground Z and applies pitch-only slope alignment. Dispatches actor updates via Actor->SetActorTransform . 

3. **Blueprint Interface** : Tuning values for VerticalInterpSpeed , VerticalDeadInterpSpeed , and performance thresholds ( LowFPSThreshold , HighFPSThreshold ). 

4. **Component Architecture** : Inherits from UMassProcessor . PostPhysics phase. 

5. **Network/Replication** : Synchronizes local actor state with replicated Mass fragments. 

### **UDetectionProcessor** 

1. **Purpose** : Handles high-level target acquisition and enemy prioritization. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

99/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : Processes UnitSignals::UnitInDetectionRange signals. Logic includes Squad target sharing (inheriting targets from squadmates). 

   - InjectCurrentTargetIfMissing ensures target persistence. Prioritizes enemies based on 

   - distance and CanAttack status. 

3. **Blueprint Interface** : ExecutionInterval (float, default 0.2s). 

4. **Component Architecture** : Inherits from UMassProcessor . PostPhysics phase. 

5. **Network/Replication** : Authoritative target logic on the Server. 

# **Mass Trait Technical Documentation** 

### **UMassActorLinkTrait** 

1. **Purpose** : Core responsibility is to facilitate the connection between Mass Entities and the Unreal Actor system by ensuring the required actor-related fragments are present on the entity template. 

2. **Implementation (CPP Analysis)** : 

   - The class overrides BuildTemplate(FMassEntityTemplateBuildContext& BuildContext, const UWorld& World) . 

   - It utilizes BuildContext.AddFragment<FMassActorFragment>() to inject the FMassActorFragment into the entity's definition. 

   - This fragment is a prerequisite for the UMassActorSubsystem to track and manage the lifecycle of an Actor associated with a specific Mass Entity. 

3. **Blueprint Interface** : As a UMassEntityTraitBase derivative, it is exposed to the MassConfig asset editor, allowing designers to add Actor Linking capabilities to entity templates via the UI. 

4. **Component Architecture** : Inherits from UMassEntityTraitBase . It does not define custom components but acts as a configuration bridge to add data fragments to the ECS-style Mass architecture. 

5. **Network/Replication** : The trait itself is a configuration object and does not replicate. The FMassActorFragment added by this trait follows standard Mass Fragment replication rules if 

configured in the Mass Entity's networking settings; however, actor-entity linking typically relies on the Actor's own replication for visual representation. 

# **Mass Traits Technical Documentation UUnitAITrait** 

1. **Purpose** : Aggregates all fragments required for an AI-controlled unit entity, including movement, avoidance, visualization, and custom game logic. 

2. **Implementation (CPP Analysis)** : In BuildTemplate , it populates the entity template with a broad set of fragments. It includes standard Mass fragments for physics ( FTransformFragment , FMassVelocityFragment ), navigation ( FMassMoveTargetFragment , 

https://wiki.teufel-engineering.com/en/rts-unit-template 

100/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

FUnitNavigationPathFragment ), and representation 

   - ( FMassRepresentationFragment ). It also adds several custom fragments for gameplay systems like patrolling, combat stats, and worker stats. The use of AddFragment is idempotent, allowing it to safely add FUnitReplicatedTransformFragment even if other traits also attempt to add it. 

3. **Blueprint Interface** : UCLASS . Inherits from UMassEntityTraitBase . 

4. **Component Architecture** : Inherits from UMassEntityTraitBase . Acts as a composite trait for unit initialization. 

5. **Network/Replication** : Explicitly adds FUnitReplicatedTransformFragment to ensure the entity can hold replicated transform data on clients. 

### **FUnitReplicatedTransformFragment** 

1. **Purpose** : Acts as a client-side buffer for transform data replicated from the server. 

2. **Implementation (CPP Analysis)** : A simple FMassFragment that holds an FTransform . This data is updated by replication processors and used by visualization systems to position entities on clients. 

3. **Blueprint Interface** : USTRUCT() . Contains UPROPERTY(Transient) FTransform Transform . 

4. **Component Architecture** : FMassFragment . 

5. **Network/Replication** : Core part of the custom replication pipeline; stores authoritative transform state on remote clients for interpolation or direct snapping. 

### **UUnitNavigationPathTrait** 

1. **Purpose** : Ensures entities have the necessary fragment to store and follow navigation paths calculated by the Mass movement system. 

2. **Implementation (CPP Analysis)** : Overrides BuildTemplate to add 

   - FUnitNavigationPathFragment to the context. This allow pathfinding processors to write 

   - navigation data to the entity and for movement processors to read from it. 

3. **Blueprint Interface** : UCLASS . Inherits from UMassEntityTraitBase . 

4. **Component Architecture** : Standard Mass Trait. 

5. **Network/Replication** : Typically navigation logic is server-authoritative; this fragment holds the path result for local simulation. 

### **UUnitMassTagTrait** 

1. **Purpose** : Applies a semantic tag to entities to identify them as "Units" within Mass queries. 

2. **Implementation (CPP Analysis)** : Adds FUnitMassTag to the entity template in BuildTemplate . This tag consumes no memory per entity and is used for efficient filtering in FMassEntityQuery to restrict processor execution to unit entities. 

3. **Blueprint Interface** : UCLASS . Inherits from UMassEntityTraitBase . 

4. **Component Architecture** : Tag-only trait. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

101/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Tags are template-level identifiers and are generally not replicated as per-entity data. 

### **UUnitReplicationTrait** 

1. **Purpose** : Configures entities for participation in the Mass Replication framework, including LOD-based relevancy and network ID management. 

2. **Implementation (CPP Analysis)** : BuildTemplate handles the setup of network-specific fragments. It checks if the world is in NM_Standalone and returns early if so. It adds mandatory replication fragments: FReplicationTemplateIDFragment (set to the template's ID), FMassNetworkIDFragment , and FMassReplicatedAgentFragment . It also adds spatial 

awareness fragments like FMassReplicationViewerInfoFragment and FMassReplicationGridCellLocationFragment , and ensures the entity is tagged with FMassInReplicationGridTag for the Mass replication grid. 

3. **Blueprint Interface** : UCLASS(MinimalAPI) . Inherits from UMassEntityTraitBase . 

4. **Component Architecture** : Specialized trait for networking integration. 

5. **Network/Replication** : Primary driver for Mass-to-Client synchronization; prepares entities for the MassReplicationProcessor . 

### **UMassActorLinkTrait** 

1. **Purpose** : Provides a mechanism to link Mass entities to their corresponding Actor representations for mixed simulation/actor setups. 

2. **Implementation (CPP Analysis)** : Overrides BuildTemplate to prepare the entity for linking with an Actor. Though the provided implementation is minimal, it defines the hook for associating AActor references with entities. 

3. **Blueprint Interface** : UCLASS . Inherits from UMassEntityTraitBase . 

4. **Component Architecture** : Base trait for entity-actor synchronization. 

5. **Network/Replication** : Essential for entities that require the presence of an Actor on clients for complex visual components or legacy systems. 

# **NavAreas Technical Documentation** 

### **UNavArea_EnergyWall** 

1. **Purpose** : Defines a specialized navigation area specifically for energy wall obstacles. Its primary responsibility is to mark regions of the NavMesh as impassable or extremely high-cost to prevent standard pathfinding from routing units through these structures. 

2. **Implementation (CPP Analysis)** : 

   - **Pathfinding Cost** : In the constructor, DefaultCost is initialized to 10000000.f . While logic elsewhere (filters) might exclude this area entirely, the extremely high cost ensures it is avoided by the A* algorithm as a fallback. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

102/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Debug Visualization** : DrawColor is set to FColor::Orange . This facilitates visual verification of the NavMesh generation in the editor or during runtime using navigation debug commands. 

3. **Blueprint Interface** : 

   - **UCLASS** : Marked with RTSUNITTEMPLATE_API , making the class accessible to other modules. It is available in the Unreal Editor for assignment to Nav Modifier components. 

4. **Component Architecture** : 

   - **Inheritance** : Subclasses UNavArea_Obstacle , inheriting standard obstacle behavior. 

   - **Constructor** : Utilizes const FObjectInitializer& ObjectInitializer to configure default object properties during the engine's class default object (CDO) creation. 

5. **Network/Replication** : As a UNavArea derivative, this class does not contain per-instance state that requires replication. Navigation data is primarily utilized by the server-side navigation system for pathfinding; clients may use it for local movement prediction if configured. 

# **NavFilters Technical Documentation** 

### **UNavFilter_Escape** 

1. **Purpose** : Provides a navigation query filter specifically designed to allow units currently positioned within a high-cost or "dirty" area (defined by UNavArea_Obstacle ) to calculate a path out of it. 

2. **Implementation (CPP Analysis)** : The implementation resides in the constructor. It utilizes the FNavigationFilterArea structure to target UNavArea_Obstacle . By setting bIsExcluded = false , it ensures the area is not an absolute barrier. It overrides TravelCostOverride and EnteringCostOverride to a relatively low value ( 5.0f ). This 

logic tricks the A* pathfinding algorithm: since entering/traveling through the obstacle is now "cheaper" than its default high cost, the pathfinder can successfully resolve a path from inside the obstacle to the nearest valid navigation polygon outside of it. 

3. **Blueprint Interface** : Exposed to the Unreal Editor via UCLASS() macro. It inherits standard UNavigationQueryFilter properties. No custom UPROPERTIES or UFUNCTIONS are 

defined, as the behavior is hard-coded in the constructor for specialized "escape" logic. 

4. **Component Architecture** : Derived from UNavigationQueryFilter . It populates the Areas array during the ObjectInitializer phase of the constructor. 

5. **Network/Replication** : Navigation filters are utilized by the NavigationSystem during pathfinding queries on the server (or client-side for predicted movement). This class contains no replicated state or RPCs. 

### **UNavFilter_Strict** 

1. **Purpose** : Enforces an absolute traversal restriction on areas marked as UNavArea_Obstacle , treating them as solid obstacles regardless of their default cost. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

103/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : In the constructor, a FNavigationFilterArea is defined for UNavArea_Obstacle . The key logic is setting bIsExcluded = true . In Unreal Engine's 

navigation system, setting bIsExcluded on a filter area tells the pathfinder to treat that specific NavArea class as null/non-traversable space for any query using this filter. 

3. **Blueprint Interface** : Exposed via UCLASS() . Inherits standard UNavigationQueryFilter functionality. No custom properties or functions are exposed. 

4. **Component Architecture** : Derived from UNavigationQueryFilter . Configuration is strictly performed within the constructor by appending the exclusion rule to the Areas array. 

5. **Network/Replication** : No network replication logic. Pathfinding using this filter is handled locally by the AI Controller's path request on the authoritative side. 

### **APlayerStartBase** 

1. **Purpose** : Extends the standard APlayerStart to serve as a configuration hub for RTS-specific player initialization. It stores team data, AI flags, and references to UI/Audio assets required at the start of a match. 

2. **Implementation (CPP Analysis)** : The implementation is currently declarative, defining data structures for other systems (like AGameMode or APlayerController ) to consume. It integrates with AWaypoint for initial unit direction and holds references to various USoundBase assets for 

standard RTS feedback (Run, Ability, Attack, etc.). It also links to widget classes 

   - ( UUnitWidgetSelector , UTaggedUnitSelector , UResourceWidget ) for UI setup during the initialization phase of the player pawn and controller. 

3. **Blueprint Interface** : 

   - SelectableTeamId (int): UPROPERTY(EditAnywhere, BlueprintReadWrite) . 

   - Team ID assigned to the player or AI spawning at this location. 

   - bIsAi (bool): UPROPERTY(EditAnywhere, BlueprintReadWrite) . Flag to indicate if 

   - an AI controller should be initialized for this player start. 

   - DefaultWaypoint (AWaypoint*): UPROPERTY(EditAnywhere, 

   - BlueprintReadWrite) . Reference to an actor used for initial pathfinding or unit assembly. 

   - WaypointSound , RunSound , AbilitySound , AttackSound , DropWorkAreaFailedSound , DropWorkAreaSound (USoundBase*): Audio cues for 

   - various RTS actions to be utilized by the PlayerController . 

   - SelectorWidget (UUnitWidgetSelector*): Pointer to the unit selection widget logic. 

   - TaggedUnitSelector (UTaggedUnitSelector*): Pointer to the tagged unit UI management logic. 

   - ResourceWidget (UResourceWidget*): Pointer to the resource display UI logic. 

4. **Component Architecture** : Inherits from APlayerStart . It does not introduce new sub-components in the header; it relies on the inherited UCapsuleComponent for collision and UArrowComponent for orientation in the editor. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

104/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Follows standard APlayerStart networking behavior. The actor is primarily used on the server during the ChoosePlayerStart phase of the AGameModeBase lifecycle. The custom properties are intended for server-side initialization of player-related classes. 

# **RTSUnitTemplate Technical Deep-Dive Documentation FRTSUnitTemplateModule** 

1. **Purpose** : Acts as the module entry point, orchestrating the lifecycle and bootstrapping the Mass Entity replication system for every world instance. 

2. **Implementation (CPP Analysis)** : 

   - StartupModule() : Subscribes to three critical engine delegates: FWorldDelegates::OnPreWorldInitialization , FWorldDelegates::OnPostWorldInitialization , and FCoreUObjectDelegates::PostLoadMapWithWorld . Each callback executes a lambda 

   - that triggers RTSReplicationBootstrap::RegisterForWorld(*World) . This multilayered approach ensures the Mass replication bubble info class is registered regardless of the world's creation context (e.g., initial load, seamless travel, or browsing). 

   - ShutdownModule() : Manages resource cleanup by unregistering the stored FDelegateHandle members ( PreWorldInitHandle , WorldInitHandle , PostLoadMapHandle ) from their respective delegates and resetting them to prevent dangling 

   - references during module unloading. 

3. **Blueprint Interface** : None. This is a native C++ module implementation of IModuleInterface and does not inherit from UObject or AActor . 

4. **Component Architecture** : Not applicable. The class serves as a singleton-like manager for module initialization and does not participate in the Actor-Component framework. 

5. **Network/Replication** : Provides the infrastructure bootstrap for the entire module's replication layer. While the module class itself is not replicated, it is responsible for ensuring that RTSReplicationBootstrap activates the Mass replication framework for networked game 

worlds. 

# **RTS Save System Technical Documentation** 

This document provides a deep-dive analysis of the save system architecture within the RTSUnitTemplate module. 

### **FCameraSaveData** 

1. **Purpose** : Persistence of the player's camera position and orientation within a level. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

105/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : A simple data structure using FVector and FRotator . It stores the absolute world transform of the camera actor at the time of saving. 

3. **Blueprint Interface** : 

   - Location : FVector (Default: ZeroVector) 

   - Rotation : FRotator (Default: ZeroRotator) 

4. **Component Architecture** : N/A (USTRUCT). 

5. **Network/Replication** : Local persistence only. 

### **FAbilitySaveData** 

1. **Purpose** : Tracks the state and availability of specific unit abilities. 

2. **Implementation (CPP Analysis)** : Uses FSoftClassPath to avoid hard references to ability classes, allowing for deferred loading. Includes an AbilityKey for integration with gating systems and booleans for manual overrides. 

3. **Blueprint Interface** : 

   - AbilityClass : FSoftClassPath (Class identifier) 

   - AbilityKey : FString (Gating system key) 

   - bOwnerDisabled : bool (Manual disable flag) 

   - bOwnerForceEnabled : bool (Manual enable override) 

4. **Component Architecture** : N/A (USTRUCT). 

5. **Network/Replication** : N/A. 

### **FUnitSaveData** 

1. **Purpose** : Primary container for capturing the complete state of an RTS unit actor for serialization. 

2. **Implementation (CPP Analysis)** : Employs FSoftClassPath for dynamic unit spawning. Captures gameplay logic state via UnitData::EState enums. It nests several sub-structs ( FLevelData , FLevelUpData , FAttributeSaveData ) and a TArray<FAbilitySaveData> to 

reconstruct complex unit actors. 

3. **Blueprint Interface** : 

   - UnitIndex : int32 (Identification index) 

   - ActorName : FString (Fallback identifier) 

   - UnitClassPath : FSoftClassPath (Spawnable class) 

   - TeamId : uint8 

   - UnitState / UnitStatePlaceholder : Enums from UnitData namespace. 

   - Location / Rotation : FVector / FRotator . 

   - Abilities : TArray<FAbilitySaveData> . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

106/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : N/A (USTRUCT). 

5. **Network/Replication** : N/A. 

### **FMapSwitchTagsForMap** 

1. **Purpose** : Manages persistent state of world triggers and event tags on a per-map basis. 

2. **Implementation (CPP Analysis)** : Uses a normalized MapKey (asset name) to index a TArray<FName> representing active environment or logic tags. 

3. **Blueprint Interface** : 

   - MapKey : FString (Normalized asset name) 

   - Tags : TArray<FName> 

4. **Component Architecture** : N/A (USTRUCT). 

5. **Network/Replication** : N/A. 

### **FWorkAreaSaveData** 

1. **Purpose** : Captures the state of interactive world actors such as construction sites, resource nodes, and capture points. 

2. **Implementation (CPP Analysis)** : Extensive data structure covering the lifecycle of a WorkArea . It tracks construction progress via BuildTime vs CurrentBuildTime , resource depletion via AvailableResourceAmount , and dynamic class associations ( WorkResourceClass , BuildingClass , etc.) using FSoftClassPath . Includes logic flags for build states 

   - ( PlannedBuilding , StartedBuilding ). 

3. **Blueprint Interface** : 

   - Tag : FString (Actor identification) 

   - WorkAreaClass : FSoftClassPath 

   - TeamId : int32 

   - Type : WorkAreaData::WorkAreaType enum. 

   - ConstructionCost : FBuildingCost struct. 

   - ControlTimer : float . 

4. **Component Architecture** : N/A (USTRUCT). 

5. **Network/Replication** : N/A. 

### **URTSSaveGame** 

1. **Purpose** : The root SaveGame object used by Unreal's UGameplayStatics system to serialize the entire game session state. 

2. **Implementation (CPP Analysis)** : Inherits from USaveGame . It acts as the aggregate root, holding arrays of units, work areas, and map-specific metadata. It records the SavedMapLongPackageName to 

https://wiki.teufel-engineering.com/en/rts-unit-template 

107/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

facilitate level-streaming or map loading upon save restoration. Includes a Unix timestamp for save ordering. 

3. **Blueprint Interface** : 

   - SavedMapLongPackageName : FString . 

   - SavedUnixTimeSeconds : int64 . 

   - CameraData : FCameraSaveData . 

   - Units : TArray<FUnitSaveData> . 

   - WorkAreas : TArray<FWorkAreaSaveData> . 

   - MapEnabledSwitchTags : TArray<FMapSwitchTagsForMap> . 

4. **Component Architecture** : UObject lifecycle, instantiated via UGameplayStatics::CreateSaveGameObject . 

5. **Network/Replication** : Not replicated. Save files are strictly local to the client/server instance performing the save operation. 

# **Subsystems Technical Documentation** 

### **UResourceVisualManager** 

1. **Purpose** : Manages the visual lifecycle and performance optimization of resources carried by units using Instanced Static Mesh (ISM) pooling. It decouples the visual representation of carried items from the Mass entities to maintain high performance during large-scale resource transport. 

2. **Implementation (CPP Analysis)** : 

   - **Initialization** : Initialize() uses a TObjectIterator to find a UResourceVisualConfig data asset within the world context, establishing global fallbacks for 

   - resource meshes and materials. 

   - **Resource Assignment** : AssignResource() implements a hierarchical lookup for visuals: 

      1. **Worker Overrides** : Checks the AWorkingUnitBase for unit-specific visual overrides. 

      2. **Resource Class Defaults** : Inspects the provided AWorkResource subclass (via CDO) for mesh/material mappings and socket offsets. 

      3. **Global Config** : Falls back to the VisualConfig assigned during initialization. 

      4. **Class Defaults** : Final fallback to the AWorkResource base class CDO. 

   - **Instance Management** : Uses GetOrCreateISM() to manage a pool of UInstancedStaticMeshComponent . New instances are added with a zero-scale transform via AddInstance() to prevent visual artifacts before the first processor update. 

   - **Hiding Logic** : RemoveResource() does not remove instances from the ISM component to avoid shifting indices for other entities. Instead, it updates the instance transform to a zero-scale transform at the origin, effectively "hiding" the instance for reuse. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

108/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Pooling Logic** : GetOrCreateISM() utilizes FMeshMaterialKey (Mesh, Material, and Shadow settings) to unique-key ISM components. It spawns a transient 

      - ResourceISMManagerActor to host these components if one does not exist. 

3. **Blueprint Interface** : 

   - 

   - **UFUNCTIONS** : 

   - AssignResource : Assigns a visual mesh to a Mass entity based on EResourceType . 

   - RemoveResource : Hides the carried resource visual for an entity. 

- **UPROPERTIES** : 

   - 

         - VisualConfig : Pointer to the UResourceVisualConfig data asset. 

      - ISMPool : A map of FMeshMaterialKey to UInstancedStaticMeshComponent 

      - for component reuse. 

4. **Component Architecture** : 

   - Inherits from UWorldSubsystem . 

   - Dynamically creates and manages UInstancedStaticMeshComponent attached to a transient manager actor. 

   - Interfaces with Mass fragments: FMassCarriedResourceFragment and FMassActorFragment . 

#### 5. **Network/Replication** : 

- Local visual management only. Relies on Mass entity state replication (e.g., resource type fragments) to trigger visual changes on clients. 

### **UUnitVisualManager** 

1. **Purpose** : Handles the instantiation and management of unit visuals for Mass entities. It maps Mass entities to pooled ISM instances and provides a lookup mechanism to retrieve AMassUnitBase actors from specific ISM instances for interaction/selection. 

2. **Implementation (CPP Analysis)** : 

   - **Visual Assignment** : AssignUnitVisual() matches a template ISM from a unit actor to a pooled ISM via GetOrCreateISM() . It implements reuse logic by checking the FMassUnitVisualFragment for existing instances that match the template or a stale pooled 

   - mesh. 

   - **Collision/Rendering Sync** : The pooled ISM inherits collision enabled status, response channels, object type (forced to ECC_WorldDynamic if static), decal reception, custom depth, and custom data float counts from the template ISM. 

   - **Socket Mapping** : Scans children of the TemplateISM for a component tagged ProjectileSpawn . If found, it caches the MuzzleOffset relative transform in the FMassUnitVisualInstance . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

109/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

- **Bidirectional Mapping** : Maintains an ISMToUnitMap 

( TMap<TWeakObjectPtr<UInstancedStaticMeshComponent>, 

      - TArray<TWeakObjectPtr<AMassUnitBase>>> ). This allows the system to resolve which AMassUnitBase is represented by a specific ISM instance index. 

   - **Visibility Control** : SetUnitVisualVisible() updates the FMassVisualEffectFragment and hides the associated ISM instances by zeroing their 

   - transforms. 

3. **Blueprint Interface** : 

   - 

      - **Public Methods (Non-UFUNCTION)** : 

      - AssignUnitVisual : Pairs a Mass entity with a template's visual representation. 

      - RemoveUnitVisual : Hides all visual instances associated with an entity and clears mappings. 

      - SetUnitVisualVisible : Toggles the visibility of unit instances. 

      - GetUnitFromInstance : Returns the AMassUnitBase pointer associated with an ISM and 

      - instance index. 

   - **UPROPERTIES** : 

      - ISMPool : Maps FMeshMaterialKey to pooled UInstancedStaticMeshComponent instances. 

4. **Component Architecture** : 

   - Inherits from UWorldSubsystem . 

   - Uses FMeshMaterialKey for deterministic component pooling. 

   - Configures ISM components with Movable mobility and disables navigation affectors. 

5. **Network/Replication** : 

   - Local-side visual representation. It is intended to run on all clients to render entities based on replicated Mass fragments. 

# **System Module Technical Documentation** 

This document provides a technical deep-dive into the core subsystems of the RTS Unit Template system module. 

### **UGameSaveSubsystem** 

1. **Purpose** : Manages the persistence of game state, including actor data (Units, WorkAreas), player camera transforms, map switch states, and level-specific metadata. 

2. **Implementation (CPP Analysis)** : 

   - **Serialization** : Iterates through TActorIterator<AUnitBase> and 

TActorIterator<AWorkArea> . It captures transforms, GAS attributes (via 

https://wiki.teufel-engineering.com/en/rts-unit-template 

110/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

UAttributeSetBase ), and ability states (via IAbilitySystemInterface ). 

   - **Map Transitions** : If a loaded save specifies a different map, it binds to FCoreUObjectDelegates::PostLoadMapWithWorld and triggers UGameplayStatics::OpenLevel . Data application is deferred until the new world is ready. 

   - **Actor Matching** : Uses a tiered approach in ApplyLoadedData . It first attempts to match existing actors via UnitIndex (for ALevelUnit ) or ActorName . If no match is found, it spawns a new instance using SavedUnit.UnitClassPath . 

   - **Mass Integration** : Synchronizes FMassMoveTargetFragment and FMassAIStateFragment to the loaded location and updates entity tags via MassUnit- 

   - >SwitchEntityTagByState . 

   - **Ability Logic** : Checks bExecuteOnLoadIfDisabled for abilities that are disabled in the save but should trigger on load. 

3. **Blueprint Interface** : 

   - UFUNCTION SaveCurrentGame(SlotName) : Primary entry point for saving. 

   - UFUNCTION LoadGameFromSlot(SlotName) : Primary entry point for loading. 

   - UFUNCTION GetAllSaveSlots() : Returns sorted list of .sav files. 

   - UFUNCTION LoadSaveSummary(...) : Retrieves metadata without fully loading the world. 

   - UPROPERTY DefaultUnitClass : Configuration for fallback spawning. 

4. **Component Architecture** : Inherits from UGameInstanceSubsystem . Singleton lifetime tied to the Game Instance. 

5. **Network/Replication** : Operates on the Server/Authority. It contains logic to mirror ability key toggles to specific clients using 

ACustomControllerBase::Client_ApplyOwnerAbilityKeyToggle to ensure UI/Local state consistency. 

### **UPlayerTeamSubsystem** 

1. **Purpose** : Maintains player-to-team associations across level travels and session reconnections. 

2. **Implementation (CPP Analysis)** : 

   - **Identity Redundancy** : Stores team IDs in three distinct maps: PendingTeams (by PlayerId ), PendingTeamsByName (by PlayerName ), and PendingTeamsByNetworkAddress . 

   - This provides robustness against PlayerId resets during transitions. 

   - **Consumption Logic** : GetTeamForPlayer includes a bConsume flag to optionally remove entries once retrieved, preventing stale data. 

3. **Blueprint Interface** : 

   - UFUNCTION SetTeamForPlayer(PC, TeamId) : Registers a player's team. 

   - UFUNCTION GetTeamForPlayer(PC, OutTeamId, bConsume) : Retrieves the 

   - registered team. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

111/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ UFUNCTION ClearAll() : Wipes all mappings. 

4. **Component Architecture** : Inherits from UGameInstanceSubsystem . 

5. **Network/Replication** : Server-side only. Used by GameMode logic to assign teams to newly joined or traveled PlayerControllers. 

### **UStoryTriggerQueueSubsystem** 

1. **Purpose** : Handles the sequential display of narrative widgets and synchronized audio playback. 

2. **Implementation (CPP Analysis)** : 

   - **Queue Management** : Uses a TArray<FStoryQueueItem> for FIFO processing. TryPlayNext is called whenever the queue is updated or a previous item finishes. 

   - **Resource Resolution** : Resolves TSoftObjectPtr for textures and materials synchronously at the moment of display. 

   - **Timers** : Uses FTimerHandle for ActiveTimerHandle (widget lifetime) and NextStoryTimerHandle (3-second delay between items). 

   - **Volume Management** : Modifies MasterSoundClass volume and calculates a GlobalSoundMultiplier based on the triggering source (Actor or Component). 

3. **Blueprint Interface** : 

   - UFUNCTION EnqueueStory(Item) : Adds a new narrative item to the queue. 

   - UFUNCTION ClearActive() : Forcibly terminates the current story item. 

   - UPROPERTY MasterSoundClass : Target for master volume control. 

4. **Component Architecture** : Inherits from UGameInstanceSubsystem . Interacts with UStoryWidgetBase and AExtendedCameraBase . 

5. **Network/Replication** : Local-only subsystem. Intended for local player UI and audio feedback. 

### **UMapSwitchSubsystem** 

1. **Purpose** : Tracks binary states ("Switch Tags") for specific maps, persisting them throughout a session. 

2. **Implementation (CPP Analysis)** : 

   - **Key Normalization** : NormalizeMapKey strips PIE prefixes ( UEDPIE_ ) and derives the asset name from long package names. 

   - **Storage** : Uses TMap<FString, TSet<FName>> for session-persistent tag storage. 

   - **Integration** : Provides ExportStateForSave and ImportStateFromSave for the UGameSaveSubsystem . 

3. **Blueprint Interface** : 

   - UFUNCTION MarkSwitchEnabledForMap(MapName, SwitchTag) : Enables a specific 

   - gameplay switch. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

112/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - UFUNCTION IsSwitchEnabledForMap(MapName, SwitchTag) : Checks if a switch is 

   - enabled. 

4. **Component Architecture** : Inherits from UGameInstanceSubsystem . 

5. **Network/Replication** : Typically runs on the Server to maintain authority over world state. 

# **RTS Unit Template Technical Documentation** 

This document provides a technical deep-dive into the unit hierarchy and class architecture of the RTS Unit Template. 

### **AGASUnit** 

1. **Purpose** : Integration point for Unreal's Gameplay Ability System (GAS), providing ability granting, activation, and queuing logic. 

2. **Implementation (CPP Analysis)** : 

   - Implements IAbilitySystemInterface to provide access to AbilitySystemComponentBase . 

   - Manages an AbilityQueue (TQueue) to handle ability requests while the ASC is busy, preventing input loss. 

   - ActivateAbilityByInputID maps EGASAbilityInputID to ability specs and handles 

   - queuing logic via QueSnapshot . 

   - InitializeAttributes applies the DefaultAttributeEffect (Gameplay Effect) to 

   - set starting stats. 

   - Uses EGameplayEffectReplicationMode::Minimal for optimized networking. 

3. **Blueprint Interface** : 

   - DefaultAbilities : Array of starting abilities. 

   - MaxAbilityQueueSize : Limit for queued ability requests. 

   - CancelCurrentAbility() : Forces termination of active ability and clears snapshots. 

   - GetAbilityDisplayObject() : Helper to retrieve proxy objects for UI display with correct 

   - costs. 

#### 4. **Component Architecture** : 

- AbilitySystemComponent : Core GAS component. 

- Attributes : UAttributeSetBase for unit statistics. 

#### 5. **Network/Replication** : 

- Replicates ASC and AttributeSet. 

- ReplicatedAbilityCosts : Syncs dynamic ability cost changes to clients. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

113/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ QueSnapshot : Mirrors the server-side queue for client-side UI prediction. 

### **ALevelUnit** 

1. **Purpose** : Manages experience progression, character leveling, and the allocation of talent points into attributes. 

2. **Implementation (CPP Analysis)** : 

   - Tick handles health and shield regeneration based on Attributes values. 

   - LevelUp_Implementation processes experience consumption and increments CharacterLevel . 

   - InvestPointInto... functions apply specialized UGameplayEffect classes to 

   - permanently modify attributes. 

   - AutoLevelUp iterates through AutolevelConfig to automatically spend points. 

   - Integrates with UTalentSaveGame for persistence. 

3. **Blueprint Interface** : 

   - LevelData : Struct containing XP, Level, and Talent/Ability points. 

   - LevelUpData : Defines XP requirements and max levels. 

   - AutolevelConfig : Array defining how points are distributed during auto-leveling. 

   - SaveLevelDataAndAttributes() : Persists unit state to a save slot. 

4. **Component Architecture** : Inherits from AGASUnit . 

5. **Network/Replication** : 

   - Replicates LevelData and LevelUpData . 

   - OnRep_LevelData triggers LevelVisibilityCheck to update UI/visuals on level-up. 

   - Investment effects are replicated via standard GAS mechanics. 

### **AAbilityUnit** 

1. **Purpose** : Intermediate class handling predefined ability sets and movement acceleration logic (e.g., for charges). 

2. **Implementation (CPP Analysis)** : 

   - TeleportToValidLocation uses LineTraceSingleByChannel for ground 

   - verification and synchronizes the Mass entity via StoredLocation . 

   - Accelerate logic uses FMath::VInterpTo to drive LaunchCharacter for smooth 

   - speed ramping during abilities. 

   - ActivateStartAbilitiesOnSpawn uses FTimerManager to defer activation, ensuring 

   - unit initialization is complete. 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

114/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - StartAbilities : Abilities activated automatically on spawn. 

   - OffensiveAbilities , DefensiveAbilities , AttackAbilities , ThrowAbilities : Classified ability buckets. 

   - SetUnitState() : Transitions unit through states like Idle , Run , Attack , etc., triggering 

   - BP events. 

   - IsWorker : Flag to toggle worker-specific state logic. 

4. **Component Architecture** : Inherits from ALevelUnit . 

5. **Network/Replication** : 

   - Replicates UnitState , UnitStatePlaceholder , and StoredUnitState to keep animation and AI logic in sync. 

### **ASpawnerUnit** 

1. **Purpose** : Base class for actors that spawn APickup objects based on probability and data table definitions. 

2. **Implementation (CPP Analysis)** : 

   - CreateSpawnDataFromDataTable parses rows into FSpawnData structs. 

   - SpawnPickupWithProbability uses FMath::RandRange (0-100) against ProbabilityArray . 

   - SpawnPickup utilizes SpawnActorDeferred to set TeamId and MaxLifeTime 

   - before finishing spawning. 

3. **Blueprint Interface** : 

   - SpawnDataTable : Reference to the definitions of items to spawn. 

   - SpawnPickupsArray() : Iterates and spawns all defined pickups. 

   - TeamId : Assigned to all spawned pickups. 

4. **Component Architecture** : Inherits from ACharacter . 

5. **Network/Replication** : 

   - Replicates TeamId , SquadId , and tags ( UnitTags , AbilitySelectionTag , TalentTag ). 

### **APathSeekerBase** 

1. **Purpose** : Basic support for Dijkstra-based navigation data storage. 

2. **Implementation (CPP Analysis)** : 

   - Stores start/end points and a FDijkstraMatrix for custom pathfinding logic. 

3. **Blueprint Interface** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

115/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - DijkstraStartPoint , DijkstraEndPoint : Path targets. 

   - FollowPath : Boolean toggle for custom movement logic. 

4. **Component Architecture** : Inherits from APerformanceUnit . 

5. **Network/Replication** : Inherits replication from parent classes. 

### **AMassUnitBase** 

1. **Purpose** : Primary bridge between standard Actors and the Mass Entity ECS, managing entity life cycles and high-performance visuals. 

2. **Implementation (CPP Analysis)** : 

   - GetMassEntityData : Robust helper to retrieve FMassEntityManager and FMassEntityHandle . 

   - SwitchEntityTagByState : Synchronizes Actor states to Mass tags (e.g., FMassStateIdleTag , FMassStateAttackTag ). 

   - Implements extensive smooth-interpolation (tweens) for ISM instances (Rotation, Location, Scale). 

   - SyncTranslation / SyncRotation : Manually pushes Actor transforms to the Mass FTransformFragment . 

#### 3. **Blueprint Interface** : 

   - MassActorBindingComponent : Handles the link between Actor and Entity. 

   - ISMComponent : Visual representation for Mass-driven units. 

   - InitializeAdditionalISM() : Allows registering extra ISM components for complex visual 

   - units. 

   - StartCharge() : High-level interface to trigger Mass-based charging movement. 

4. **Component Architecture** : 

   - UMassActorBindingComponent : Manages entity binding. 

   - UInstancedStaticMeshComponent : Main visual. 

   - USelectionDecalComponent : Selection indicator. 

   - UWidgetComponent : Two components for Health and Timer bars. 

#### 5. **Network/Replication** : 

- Replicates visual effect parameters ( Rep_VE_... ) for pulsate, rotate, oscillate, and dish-rotation effects. 

- Uses NetMulticast to trigger linear visual transitions on all clients. 

### **APerformanceUnit** 

1. **Purpose** : Optimized handling of visual/audio effects, visibility logic (Fog of War), and shared squad UI. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

116/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

#### 2. **Implementation (CPP Analysis)** : 

   - ComputeLocalVisibility : Core logic for Fog of War, checking initialization, invisibility tags, 

   - and viewport status. 

   - FireEffects : Spawns Niagara/Audio with delays, tracking them in ActiveNiagara and ActiveAudio arrays for cleanup. 

   - HandleSquadHealthBarVisibility : Logic to determine if this unit is the "Squad Leader" 

   - responsible for rendering the shared healthbar. 

   - IMassVisibilityInterface : Overrides for Mass-driven visibility updates. 

3. **Blueprint Interface** : 

   - DeadVFX , MeleeImpactVFX : Visual effect references. 

   - FireEffectsAtLocation() : Utility to spawn visual/audio at specific points with kill delays. 

   - StopAllEffects() : Instant cleanup of all tracked transient effects. 

4. **Component Architecture** : Inherits from AMassUnitBase . Manages transient arrays for ActiveNiagara and ActiveAudio . 

5. **Network/Replication** : 

   - Replicates effect parameters (Scale, Sound, Delays) and IsInitialized . 

   - MulticastSetEnemyVisibility : Logic for team-based detection synchronization. 

### **AUnitBase** 

1. **Purpose** : The foundational class for all units, combining GAS, Mass, AI, and combat logic. 

2. **Implementation (CPP Analysis)** : 

   - SetHealth : Authoritative health management with 25%/50% threshold events for BP feedback. 

   - SpawnProjectileFromClass : Complex multi-projectile logic supporting Homing 

   - (spirals/interp), Twin-shots (side-by-side), and Spread. Supports both standard Actors and Mass Projectiles. 

   - GetProjectileSpawnLocation : Searches for components tagged "ProjectileSpawn" before 

   - falling back to calculated offsets. 

   - SpawnUnitsFromParameters : Advanced factory method for dynamic unit spawning 

   - (summons, squads). 

   - Multicast_RegisterBuildingAsObstacle : Dynamic NavMesh modification using a 

   - spawned proxy actor. 

3. **Blueprint Interface** : 

   - UnitToChase , FollowUnit , NextWaypoint : Navigation and targeting targets. 

   - ProjectileBaseClass : Class to spawn for attacks. 

   - ApplyFollowTarget() : Command for friendly follow behavior. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

117/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

▸ AddUnitToChase() : Interface for sensory input (detection). 

#### 4. **Component Architecture** : 

   - Inherits from AWorkingUnitBase . 

   - Contains core GAS components, two Niagara components for build/generic effects, and cached references to BoxCollisionComponent . 

5. **Network/Replication** : 

   - Replicates combat state flags: CanAttack , bHoldPosition , bIsInvisible . 

   - IncrementMassProjectileFireCounter : Minimal overhead replication for high-frequency 

   - shooting via Mass. 

### **AWorkingUnitBase** 

1. **Purpose** : Implements resource gathering, construction site management, and worker-specific visual management. 

2. **Implementation (CPP Analysis)** : 

   - SpawnWorkAreaReplicated : Handles snapping logic for Extension areas using EExtensionSnapMethod (Snap 1, 2, 4, 8 way). 

   - OnRep_CarryingResourceType : Uses UResourceVisualManager to update the unit's 

   - visual entity based on what it is carrying. 

   - Manages the lifecycle of AWorkArea and AWorkResource . 

3. **Blueprint Interface** : 

   - ResourcePlace : Target resource area. 

   - BuildArea : Target construction area. 

   - ResourceExtractionTime : Speed of gathering. 

   - Niagara_Build : Visual effect for building state. 

4. **Component Architecture** : Inherits from ATransportUnit . 

5. **Network/Replication** : 

   - Replicated props: CurrentDraggedWorkArea , ResourcePlace , Base , BuildArea , CarryingResourceType . 

### **ATransportUnit** 

1. **Purpose** : Logic for vehicles or structures that can load and transport other units. 

2. **Implementation (CPP Analysis)** : 

   - LoadUnit : Validates TeamId , TransportId , and UnitSpaceNeeded before adding to LoadedUnits . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

118/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - UnloadNextUnit : Uses FTimerManager for gradual unloading. Performs a LineTraceSingleByChannel to find safe ground for the unit. 

   - MulticastApplyLoadEffects / MulticastApplyUnloadEffects : Synchronizes 

   - visual and collision state for units entering/exiting transport (toggling visibility in Mass and Actors). 

3. **Blueprint Interface** : 

   - IsATransporter : Flag to enable logic. 

   - MaxTransportUnits , MaxSpacePerUnitAllowed : Capacity constraints. 

   - UnloadInterval : Delay between units exiting. 

4. **Component Architecture** : Inherits from APathSeekerBase . Binds logic to CapsuleComponent overlaps. 

5. **Network/Replication** : 

   - Replicates LoadedUnits , CurrentUnitsLoaded , and transport configuration. 

### **ABuildingBase** 

1. **Purpose** : Stationary units used for resource drop-off, base building, and territorial control. 

2. **Implementation (CPP Analysis)** : 

   - SwitchResourceArea : Intelligent worker redistribution logic that filters available AWorkArea 

   - by distance using a multiplier. 

   - SpawnEnergyWall : Creates connections between buildings (Origins and Extensions). 

   - IsLocationInBeaconRange : Utility to check if a location is covered by territorial beacons. 

3. **Blueprint Interface** : 

   - IsBase : Flag to act as a resource drop-off point. 

   - BeaconRange : Radius for territorial coverage. 

   - ExtensionSnapMethod : Snapping behavior for building extensions. 

   - SetEnergyWallsActive() : Toggles connections. 

4. **Component Architecture** : Inherits from AUnitBase . Manages internal array of AEnergyWall actors. 

5. **Network/Replication** : 

   - Replicates EnergyWallArray . 

   - Uses MulticastRotateNiagaraToOrigin for orienting construction effects. 

### **AConstructionUnit** 

1. **Purpose** : Represents a visual and logical placeholder for a building currently under construction. 

2. **Implementation (CPP Analysis)** : 

https://wiki.teufel-engineering.com/en/rts-unit-template 

119/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - Drives complex visual animations (Spin, Oscillation, Pulsation) directly into Mass FMassVisualEffectFragment . 

   - ResolveVisualComponent : Finds appropriate mesh component for animations. 

   - KillConstructionUnit : Authoritative cleanup upon completion or destruction. 

3. **Blueprint Interface** : 

   - Worker : The unit assigned to build. 

   - WorkArea : The area being built. 

   - ScaleZ : If true, matches visual Z scale to the WorkArea bounds. 

4. **Component Architecture** : Inherits from AUnitBase . 

5. **Network/Replication** : 

   - Replicates Worker and WorkArea . 

   - Uses NetMulticast to trigger and synchronize visual animation states across clients. 

### **AHealingUnit** 

1. **Purpose** : Specialized support unit logic for target selection and healing actor management. 

2. **Implementation (CPP Analysis)** : 

   - SetNextUnitToChaseHeal : Filters UnitsToChase for units with Health < 

   - MaxHealth , prioritizing the lowest health value within the SightRadius . 

   - SpawnHealActor : Spawns a dedicated actor at the target's location with configurable scale and 

   - offset. 

3. **Blueprint Interface** : 

   - HealingActorBaseClass : Class of the healing effect actor. 

   - HealActorScale , HealActorSpawnOffset : Visual configuration. 

   - SetNextUnitToChaseHeal() : Logic trigger for AI support behavior. 

4. **Component Architecture** : Inherits from AUnitBase . 

5. **Network/Replication** : Uses MultiCastStartHealingEvent to synchronize visual healing triggers. 

### **ASpeakingUnit** 

1. **Purpose** : Units that interact with story triggers via speech bubbles and localized audio. 

2. **Implementation (CPP Analysis)** : 

   - PlaySoundOnce : Utility with cooldown to prevent audio overlap. Integrates with UStoryTriggerQueueSubsystem for global volume control. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

120/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - Manages SpeechBubble widget state and visibility based on distance. 

3. **Blueprint Interface** : 

   - Text_Id : ID for data table lookup of speech strings. 

   - SpeechVolume , BackgroundVolume : Audio levels. 

   - SpeechBubbleWidgetCompLocation : Placement for the bubble. 

4. **Component Architecture** : Inherits from AUnitBase . Contains a UWidgetComponent for USpeechBubble . 

5. **Network/Replication** : Inherits replication from AUnitBase . 

# **Units Module: Technical Deep Dive** 

This document provides a detailed technical analysis of the unit classes within the RTS Unit Template, focusing on their implementation, interface for designers, and architectural composition. 

### **AUnitBase** 

1. **Purpose** : The foundational class for all units and buildings in the template. It serves as the primary interface for combat logic (projectile spawning, damage handling), squad management, and world-space navigation feedback (NavMesh obstacle registration). 

2. **Implementation (CPP Analysis)** : 

   - **Combat** : HandleProjectileImpact_Implementation calculates final damage by subtracting Armor/Magic Resistance from the projectile's base damage or attacker's attributes. It uses ApplyInvestmentEffect to trigger secondary status effects. 

   - **Navigation** : Multicast_RegisterBuildingAsObstacle_Implementation dynamically blocks the NavMesh. It spawns a proxy actor containing a UBoxComponent and UNavModifierComponent set to UNavArea_Obstacle , then notifies the UNavigationSystemV1 to dirty the area. 

   - **Projectile Spawning** : GetProjectileSpawnLocation implements a fallback logic: it first searches for a component tagged ProjectileSpawn . If missing, it queries Mass visual instances for a bHasMuzzle flag, otherwise it calculates an offset based on the unit's forward vector and ProjectileSpawnOffset . 

3. **Blueprint Interface** : 

   - **Properties** : FollowUnit (Unit to track), CanMove , UnitIcon , Name , Type , CanAttack , bHoldPosition . 

   - **Functions** : SpawnProjectileFromClass (Spawns a projectile targeting an actor), SetWaypoint (Assigns a patrol path), IsSquadHealthbarOwner (Determines if this unit 

   - renders the group health bar). 

https://wiki.teufel-engineering.com/en/rts-unit-template 

121/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Initialized in the constructor with AbilitySystemComponent (replicated, minimal mode), Attributes (AttributeSet), and two UNiagaraComponent s ( Niagara_A , Niagara_B ) for persistent effects. It forces GetCharacterMovement()- 

   - >SetIsReplicated(false) to offload movement to the Mass system. 

5. **Network/Replication** : Replicates combat status ( CanAttack , UnitToChase ), asset paths ( MeshAssetPath , MeshMaterialPath ), and navigation data. Uses Reliable RPCs for gameplaycritical events like ServerStartAttackEvent . 

### **AConstructionUnit** 

1. **Purpose** : A specialized unit representing a building in progress. It acts as a visual proxy for construction sites, providing animations like oscillation or scale pulsation to indicate work. 

2. **Implementation (CPP Analysis)** : 

   - **Visual Logic** : It utilizes FMassVisualEffectFragment to run animations efficiently on the client. MulticastStartRotateVisual_Implementation sets flags in this fragment to trigger rotation logic in Mass processors. 

   - **Pulsation Math** : MulticastPulsateScale_Implementation captures the current base scale of the ISMComponent and calculates min/max bounds based on MinMultiplier and MaxMultiplier . 

   - **Termination** : KillConstructionUnit provides a clean way to zero health and hide the site immediately via a Server RPC. 

3. **Blueprint Interface** : 

   - **Properties** : Worker (Assigned construction unit), WorkArea (Associated build site), ScaleZ (Flag to match work area height), PulsateMinMultiplier/MaxMultiplier . 

   - **Functions** : MulticastStartRotateVisual , MulticastStartOscillateVisual , MulticastPulsateScale . 

4. **Component Architecture** : Inherits from AUnitBase . It is optimized for stationarity ( CanMove = false ). 

5. **Network/Replication** : Replicates its Worker and WorkArea references to ensure all clients know which unit is building which site. 

### **ATransportUnit** 

1. **Purpose** : Manages the loading, unloading, and containment of units within a transport actor. 

2. **Implementation (CPP Analysis)** : 

   - **Loading** : LoadUnit validates the TransportId , TeamId , and UnitSpaceNeeded . It calls MulticastApplyLoadEffects which adds the FMassStateStopMovementTag to the unit's entity and hides its visuals via the UUnitVisualManager . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

122/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - **Unloading** : UnloadNextUnit runs on a timer ( UnloadInterval ). It calculates a random position within UnloadVariationMin/Max and uses LineTraceSingleByChannel to find the ground. It calls UpdateEntityStateOnUnload to set the unit's StoredLocation and MoveTarget in Mass. 

3. **Blueprint Interface** : 

   - **Properties** : IsATransporter , MaxTransportUnits , InstantLoadRange , UnloadOffset , UnitSpaceNeeded (for the transported unit). 

   - **Functions** : LoadUnit , UnloadAllUnits , SetRdyForTransport . 

4. **Component Architecture** : Inherits from APathSeekerBase . It uses its root capsule for detection if BindTransportOverlap is called. 

5. **Network/Replication** : Replicates the LoadedUnits array and CurrentUnitsLoaded count. Uses Reliable Multicasts ( MulticastApplyLoadEffects , MulticastApplyUnloadEffects ) to sync unit visibility and collision states. 

### **AGASUnit** 

1. **Purpose** : Integrates the Gameplay Ability System (GAS) into the unit hierarchy, providing support for ability queuing and attribute replication. 

2. **Implementation (CPP Analysis)** : 

   - **Ability Queuing** : ActivateAbilityByInputID checks ActivatedAbilityInstance . If busy, it adds the request to a TQueue<FQueuedAbility> . 

      - ActivateNextQueuedAbility is triggered via OnAbilityEnded or a fallback timer. 

   - **Attribute Initialization** : InitializeAttributes applies the DefaultAttributeEffect (GameplayEffect) to set base stats. It also calls UGameplayAbilityBase::ApplyActiveUpgradesToUnit to inject global upgrades. 

   - **Interaction** : FireMouseHitAbility maps mouse clicks to target locations inside the unit's FMassAITargetFragment , allowing abilities to use world-space targets. 

3. **Blueprint Interface** : 

   - **Properties** : AbilitySystemComponent , Attributes , DefaultAbilities , AbilityQueueSize , MaxAbilityQueueSize . 

   - **Functions** : ActivateAbilityByInputID , CancelCurrentAbility , GetAbilityDisplayObject (Returns a proxy with the correct current cost). 

4. **Component Architecture** : Composed of UAbilitySystemComponentBase and UAttributeSetBase . 

5. **Network/Replication** : Replicates the ASC and Attributes. ReplicatedAbilityCosts syncs dynamic cost overrides to clients for accurate UI representation. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

123/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

### **APerformanceUnit** 

1. **Purpose** : A technical layer dedicated to performance optimization and client-side feedback (Fog of War, VFX/SFX pooling, and UI management). 

2. **Implementation (CPP Analysis)** : 

   - **Visibility** : Implements IMassVisibilityInterface . SetEnemyVisibility uses SelectableTeamId from the local ACustomControllerBase to determine if an enemy 

   - should be rendered based on fog settings. 

   - **Effect Management** : FireEffects manages a pool of ActiveNiagara and ActiveAudio components. It uses FTimerDelegate::CreateLambda with TWeakObjectPtr<APerformanceUnit> to safely handle delayed impact effects even if the 

   - actor is destroyed. 

   - **UI Optimization** : HandleSquadHealthBarVisibility logic ensures only one unit per SquadId renders the USquadHealthBar widget, reducing Slate draw calls significantly in large 

   - groups. 

3. **Blueprint Interface** : 

   - **Properties** : MeleeImpactVFX , DeadSound , IsOnViewport , EnableFog , HideHealthBarUnitCount . 

   - **Functions** : FireEffects , StopAllEffects , CheckHealthBarVisibility . 

4. **Component Architecture** : Inherits from AMassUnitBase . 

5. **Network/Replication** : Replicates feedback references ( MeleeImpactVFX , DeadSound , etc.) and visibility-related flags like StopVisibilityTick and AbilityIndicatorVisibility . 

# **Widgets Technical Documentation** 

### **UMapSwitchWidget** 

1. **Purpose** : Facilitates player confirmation for level transitions (map travel) via interactive actors. 

2. **Implementation (CPP Analysis)** : Logic uses UMapSwitchSubsystem to persist cross-map state. OnYesClicked calls MarkSwitchEnabledForMap to unlock the destination tag before 

invoking Server_TravelToMap on the player controller. InitializeWidget dynamically adjusts visibility of Yes/No vs. OK buttons based on the Enabled state of the switch. 

3. **Blueprint Interface** : InitializeWidget(FString MapName, AMapSwitchActor* OwningActor, bool Enabled) . Widget bindings: DialogText , YesButton , NoButton , OkButton . 

4. **Component Architecture** : Subclass of UUserWidget . NativeConstruct performs dynamic binding of button delegates. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

124/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

5. **Network/Replication** : Operates on the client; triggers Server_TravelToMap RPC on the serverowned Player Controller to initiate seamless or non-seamless travel. 

### **UStoryWidgetBase** 

1. **Purpose** : Provides a letter-by-letter "typewriter" text reveal system with support for background images or materials. 

2. **Implementation (CPP Analysis)** : Uses a FTimerHandle ( RevealTimerHandle ) and UpdateTextOnce to increment RevealedCount . NativeTick handles an optional blinking 

cursor using GetWorld()->GetTimeSeconds() modulo math. Supports fallback UI generation in NativeConstruct using WidgetTree->ConstructWidget if bindings are missing. 

3. **Blueprint Interface** : StartStory , ResetStory , RevealAll . Properties: CharactersPerSecond , CursorType (Enum), DefaultText , DefaultImage , DefaultMaterial . 

4. **Component Architecture** : Uses UBorder , UTextBlock , and UImage bindings. Employs UVerticalBox for dynamic layout construction. 

5. **Network/Replication** : Local UI purely. 

### **USquadHealthBar** 

1. **Purpose** : Aggregates health, shield, and level data across all units belonging to a specific SquadId and TeamId . 

2. **Implementation (CPP Analysis)** : Overrides UpdateWidget to perform an actor iteration ( TActorIterator<AUnitBase> ) across the world. ComputeSquadHealth sums attributes of all valid, living squad members. Uses AsyncTask(ENamedThreads::GameThread) to ensure UI updates occur on the main thread if triggered externally. 

3. **Blueprint Interface** : Inherits from UUnitBaseHealthBar . bAlwaysShowSquadHealthbar property. 

4. **Component Architecture** : Extension of UUnitBaseHealthBar . 

5. **Network/Replication** : Aggregates data from replicated attributes of units present in the client's world. 

### **UTalentChooser** 

1. **Purpose** : UI for managing character leveling and stat-based talent point allocation. 

2. **Implementation (CPP Analysis)** : Maps OwnerUnitBase->Attributes (Stamina, AttackPower, etc.) to a series of ProgressBars. UpdateProgressBars calculates percentage based on LevelUpData.MaxTalentsPerStat . Uses a timer ( UpdateTimerHandle ) for polling 

updates via UpdateWidget . 

3. **Blueprint Interface** : StartUpdateTimer , StopTimer , UpdateWidget , UpdateProgressBars , InitializeAttributes , UpdateExperience , UpdateLevelAndTalents , CreateClassUIElements , InitializeLevelAndTalentUI , HandleTalentButtonClicked , 

https://wiki.teufel-engineering.com/en/rts-unit-template 

125/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

OnLevelUpClicked , OnResetTalentsClicked . Bindings: 

ExperienceProgressBar , CurrentLevel , AvailableTalents . 

4. **Component Architecture** : Stores attribute pointers in TArray<FGameplayAttributeData*> . Dynamically retrieves UI components by name string (e.g., "ProgressBar_%d"). 

5. **Network/Replication** : Interaction triggers LevelUp() and ResetTalents() on the ALevelUnit (which handles server-side logic). 

### **UDamageIndicator** 

1. **Purpose** : World-space floating text showing damage values with visual scaling and fading. 

2. **Implementation (CPP Analysis)** : Calculates opacity via linear decrement per tick. CalculateTextSize and CalculateTextColor use FMath::Clamp and Alpha 

interpolation (Lerp) to scale font size and color between MinDamage and MaxDamage thresholds. 

3. **Blueprint Interface** : SetDamage , SetColour . Properties: IndicatorFont , MaxUnitCount , UpdateInterval . 

4. **Component Architecture** : Polling-based update via StartUpdateTimer . 

5. **Network/Replication** : Local cosmetic effect; spawned based on damage events received by the client. 

### **UResourceWidget** 

1. **Purpose** : Displays team-wide resource stockpiles and worker assignments. 

2. **Implementation (CPP Analysis)** : Retrieves data from AResourceGameState . PopulateResourceList iterates through TeamResources and instantiates UResourceEntryWidget instances. UpdateWidget uses a TMap<EResourceType, 

const FResourceArray*> for _O_ (1) lookup performance when syncing UI to game state. 

3. **Blueprint Interface** : SetTeamId , StartUpdateTimer , StopTimer . Configuration: ResourceIcons , ResourceDisplayNames , ResourceWorkerUICollapseOverrides . 

4. **Component Architecture** : Parent container for UResourceEntryWidget . Uses UPanelWidget for child management. 

5. **Network/Replication** : Syncs UI state with replicated FResourceArray data from the GameState. 

### **UUnitTimerWidget** 

1. **Purpose** : Visualizes progress for unit-specific actions (Casting, Building, Repairing, Transporting). 

2. **Implementation (CPP Analysis)** : Switches logic based on UnitBase->GetUnitState() . For UnitData::Casting , it calculates percent via UnitControlTimer / CastTime . For IsATransporter , it displays CurrentUnitsLoaded / MaxTransportUnits . 

3. **Blueprint Interface** : SetOwnerActor , TimerTick . Bindings: TimerBar , TransportText . Configuration: CastingColor , BuildColor , TransportColor , etc. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

126/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Ticking widget with a TWeakObjectPtr to the owner unit to prevent memory leaks if the unit is destroyed. 

5. **Network/Replication** : Progress is driven by replicated timer variables on the unit. 

### **USoundControlWidget** 

1. **Purpose** : Provides a bridge between UI sliders and the UStoryTriggerQueueSubsystem for volume management. 

2. **Implementation (CPP Analysis)** : Wrappers around UStoryTriggerQueueSubsystem getters and setters for Master and Default Sound volumes. Accesses subsystem via UGameInstance . 

3. **Blueprint Interface** : SetDefaultSoundVolume , GetDefaultSoundVolume , SetMasterVolume , GetMasterVolume . 

4. **Component Architecture** : Stateless utility widget. 

5. **Network/Replication** : Local client settings. 

### **USpeechBubble** 

1. **Purpose** : Advanced dialogue system supporting branching paths, audio playback, and animation timings. 

2. **Implementation (CPP Analysis)** : Consumes UDataTable rows ( FSpeechData_Texts and FSpeechData_Buttons ). SetTableDataId populates text and sets up button targets. OnClick advances state machine WidgetIndex . Handles UAudioComponent for speech 

and background tracks. 

3. **Blueprint Interface** : SetTableDataId , PlayButtonSound , SwitchWidget . Bindings: Text , Button_1 through Button_4 , WidgetSwitcher . 

4. **Component Architecture** : Integrated with USpeechButton . Uses UWidgetSwitcher to toggle between dialogue states. 

5. **Network/Replication** : Local UI interaction. 

### **ULoadingWidget** 

1. **Purpose** : Displays game initialization progress. 

2. **Implementation (CPP Analysis)** : NativeTick calculates progress by comparing GetServerWorldTimeSeconds() against ServerWorldTimeStart . Auto-destructs via RemoveFromParent() when Elapsed >= TotalDuration . 

3. **Blueprint Interface** : SetupLoadingWidget(float Duration, float StartTime) . Binding: LoadingBar . 

4. **Component Architecture** : Minimalist ticking widget. 

5. **Network/Replication** : Uses replicated server time to ensure progress synchronization across clients. 

### **UWinConditionWidget** 

1. **Purpose** : Detailed dashboard showing map objectives and current progress. 

https://wiki.teufel-engineering.com/en/rts-unit-template 

127/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

2. **Implementation (CPP Analysis)** : Connects to AWinLoseConfigActor . UpdateConditionText implements a large switch for EWinLoseCondition 

   - (TaggedUnitsDestroyed, ResourceCount, etc.). Uses RichTextBlock for icon injection. SplitPascalCase utility cleans up tag names for display. 

3. **Blueprint Interface** : StartUpdateTimer , StopTimer . Bindings: ConditionText , RichConditionText , numerous resource icon/text pairs. 

4. **Component Architecture** : Polling-based update synchronized via UpdateTimerHandle . 

5. **Network/Replication** : Displays data from the replicated AWinLoseConfigActor . 

### **USpawnEnergyBar** 

1. **Purpose** : Visualizes energy levels for unit production platforms. 

2. **Implementation (CPP Analysis)** : Polling tick updates EnergyBar percent using GetEnergy() / GetMaxEnergy() . 

3. **Blueprint Interface** : SetOwnerActor , GetOwnerActor , TimerTick . Bindings: EnergyBar , CurrentEnergyLabel , MaxEnergyLabel . 

4. **Component Architecture** : Tied to AUnitSpawnPlatform . 

5. **Network/Replication** : Reflects replicated energy values from the platform actor. 

### **USpeechButton** 

1. **Purpose** : Interactive button within a speech bubble to trigger dialogue transitions. 

2. **Implementation (CPP Analysis)** : Overrides OnClick to broadcast CallbackTableDelegate . SetTableDataId invokes PlayButtonSound and updates the parent USpeechBubble . 

3. **Blueprint Interface** : New_Text_Id , SpeechBubble reference. 

4. **Component Architecture** : Custom UButton subclass. 

5. **Network/Replication** : Client-side interaction. 

### **UTaggedUnitSelector** 

1. **Purpose** : Manage group selection UI for units assigned to specific hotkey tags. 

2. **Implementation (CPP Analysis)** : InitWidget builds a TMap between UTaggedUnitButton instances and ACustomControllerBase tag properties (e.g., KeyTagCtrl1 ). Centralizes click handling via HandleTaggedUnitButtonClicked . 

3. **Blueprint Interface** : InitWidget . Bindings for 16 specific tag buttons (Ctrl1-6, Alt1-6, Ctrl QWER). 

4. **Component Architecture** : Orchestrator for UTaggedUnitButton components. 

5. **Network/Replication** : Triggers SelectUnitsWithTag on the controller (local/server logic). 

### **UControlWidget** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

128/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Option menu for toggling camera and control preferences. 

2. **Implementation (CPP Analysis)** : Directly modifies ACameraBase->SwapScroll and ACustomControllerBase->SwapAttackMove . Syncs UCheckBox state in NativeConstruct . 

3. **Blueprint Interface** : Bindings: SwapScrollCheckBox , SwapAttackMoveCheckBox . 

4. **Component Architecture** : Logic-heavy UI controller. 

5. **Network/Replication** : Persists settings locally to the player's controller/pawn. 

### **UMapMarkerWidget** 

1. **Purpose** : Simple world-space label. 

2. **Implementation (CPP Analysis)** : Wrapper for UTextBlock::SetText . 

3. **Blueprint Interface** : SetMarkerText . Binding: MarkerText . 

4. **Component Architecture** : Lightweight widget for UWidgetComponent usage. 

5. **Network/Replication** : Client-side visual. 

### **UTaggedUnitButton** 

1. **Purpose** : Individual button representing a gameplay tag group. 

2. **Implementation (CPP Analysis)** : Broadcasts OnClicked delegate with its associated FGameplayTag . SetIcon updates IconImage brush. 

3. **Blueprint Interface** : SetIcon . Bindings: MainButton , IconImage . 

4. **Component Architecture** : Atomic component for UTaggedUnitSelector . 

5. **Network/Replication** : Local UI interaction. 

### **UAbilityButton** 

1. **Purpose** : HUD button for selecting unit abilities, handling selection logic and permissions. 

2. **Implementation (CPP Analysis)** : Validates selection against CDO flags ( bDisabled ) and UGameplayAbilityBase team/owner keys (ForceEnabled vs Disabled). Implements precedence: 

OwnerForce > OwnerDisable > TeamForce. 

3. **Blueprint Interface** : OnClick , SetAbility . Property: Id . 

4. **Component Architecture** : Custom UButton that interacts with AExtendedControllerBase . 

5. **Network/Replication** : Local validation before pushing ability classes into unit arrays. 

### **UMapMenuWidget** 

1. **Purpose** : Main menu interface for level selection and quitting. 

2. **Implementation (CPP Analysis)** : Uses TSoftObjectPtr<UWorld> for map references. OnMap1Clicked resolves the long package name and calls Server_TravelToMap . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

129/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

3. **Blueprint Interface** : Map1Name , Map2Name . Bindings: Map1Button , Map2Button , ExitButton . 

4. **Component Architecture** : Uses UKismetSystemLibrary::QuitGame for exit functionality. 

5. **Network/Replication** : Triggers server-side travel via Player Controller. 

### **USaveGameWidget** 

1. **Purpose** : UI for managing game save/load operations and viewing existing slots. 

2. **Implementation (CPP Analysis)** : Interfaces with UGameSaveSubsystem . PopulateSavesList uses UGameSaveSubsystem to find and display save slots. LoadSaveSummary is used to display metadata (Map name, Timestamp). 

3. **Blueprint Interface** : InitializeWidget , HandleSlotItemClicked . Bindings: SlotNameTextBox , SavedSlotsList (ScrollBox), YesButton , NoButton , LoadButton . 

4. **Component Architecture** : Uses WidgetTree->ConstructWidget for dynamic list population. 

5. **Network/Replication** : Save operations are typically handled by the server or local host via the subsystem. 

### **USaveSlotListItemWidget** 

1. **Purpose** : Individual entry in the save game list. 

2. **Implementation (CPP Analysis)** : Binds OnSelectClicked to notify the USaveGameWidget parent. 

3. **Blueprint Interface** : InitializeItem . Bindings: SelectButton , LabelText . 

4. **Component Architecture** : Child widget of USaveGameWidget . 

5. **Network/Replication** : Client-side UI. 

### **UUnitWidgetSelector** 

1. **Purpose** : Primary HUD component for managing multiple selected units, their abilities, and cooldowns. 

2. **Implementation (CPP Analysis)** : Orchestrates visibility of selection buttons based on SquadId (grouping). SetButtonLabelCount generates sequential indexing (e.g., "0 / 1 / 2"). UpdateAbilityCooldowns polls the server via Server_RequestCooldown . UpdateCurrentAbility visualizes active casting snapshots. 

3. **Blueprint Interface** : InitWidget , ReplaceRarityKeywords , UpdateSelectedUnits , SetWidgetCooldown , UpdateAbilityCooldowns , UpdateAbilityButtonsState , UpdateCurrentAbility , UpdateQueuedAbilityIcons , OnAbilityQueueButtonClicked , OnCurrentAbilityButtonClicked , ChangeAbilityButtonCount , GetButtonsFromBP , SetButtonColours , SetButtonIds , SetVisibleButtonCount , SetButtonLabelCount , SetUnitIcons . 

https://wiki.teufel-engineering.com/en/rts-unit-template 

130/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

4. **Component Architecture** : Complex orchestrator managing multiple arrays of child widgets 

   - ( SingleSelectButtons , AbilityQueIcons , etc.). 

5. **Network/Replication** : Heavily reliant on replicated unit state and RPCs for cooldown synchronization. 

### **UUnitBaseHealthBar** 

1. **Purpose** : Base class for unit overhead health and resource bars. 

2. **Implementation (CPP Analysis)** : Calculates health/shield percentages from Attributes . UpdateExperience calculates XP bar fill based on LevelUpData.ExperiencePerLevel . 

Includes ResetCollapseTimer logic to hide the widget after inactivity. 

3. **Blueprint Interface** : SetOwnerActor , UpdateExperience , ResetCollapseTimer , CollapseWidget , UpdateWidget . Bindings: HealthBar , ShieldBar , CurrentHealthLabel , CharacterLevel , etc. 

4. **Component Architecture** : Designed for UWidgetComponent usage. 

5. **Network/Replication** : Polled on client; reads from replicated unit attributes. 

### **USaveSlotClickHandler** 

1. **Purpose** : Helper object to bridge dynamic button clicks to save slot logic. 

2. **Implementation (CPP Analysis)** : Stores a SlotName and calls HandleSlotItemClicked on the USaveGameWidget when HandleClick is triggered. 

3. **Blueprint Interface** : Internal UFUNCTION HandleClick . 

4. **Component Architecture** : UObject based utility, not a widget. 

5. **Network/Replication** : Local memory management. 

### **UGameTimerWidget** 

1. **Purpose** : HUD timer showing elapsed match time. 

2. **Implementation (CPP Analysis)** : NativeTick calculates difference between GetServerWorldTimeSeconds() and AResourceGameState::MatchStartTime . 

Formats result as MM:SS . 

3. **Blueprint Interface** : Binding: GameTime . 

4. **Component Architecture** : Simple ticking widget. 

5. **Network/Replication** : Uses replicated GameState time variables. 

### **UMinimapWidget** 

1. **Purpose** : Interactive minimap with coordinate projection and camera control. 

2. **Implementation (CPP Analysis)** : NativeTick counter-rotates the map based on CameraBase>SpringArmRotator.Yaw . MoveCameraToMinimapLocation uses 2D rotation math to transform local widget clicks into world XY, then performs a ground trace 

https://wiki.teufel-engineering.com/en/rts-unit-template 

131/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

   - ( LineTraceSingleByChannel ) for Z-level adjustment. Supports Right-Click move commands via ACustomControllerBase . 

3. **Blueprint Interface** : InitializeForTeam . Binding: MinimapImage . 

4. **Component Architecture** : Uses dynamic material parameters ( TopographyTexture , MinimapTexture ) for rendering. 

5. **Network/Replication** : Interaction triggers camera updates and move RPCs. 

### **UResourceEntryWidget** 

1. **Purpose** : Individual resource row in the HUD. 

2. **Implementation (CPP Analysis)** : SetResourceData handles formatting for "Supply" (e.g., "10 / 100") vs. standard resources. UpdateWorkerCount performs local string-to-int math to update display. 

3. **Blueprint Interface** : UpdateWorkerCount , SetResourceData . Bindings: ResourceNameText , ResourceAmountText , WorkerCountText , AddWorkerButton , RemoveWorkerButton . 

4. **Component Architecture** : Atomic component used by UResourceWidget . 

5. **Network/Replication** : Local representation of replicated resource counts. 

### **UWinLoseWidget** 

1. **Purpose** : Post-game screen for Victory/Defeat. 

2. **Implementation (CPP Analysis)** : Sets input mode to FInputModeUIOnly . OnOkClicked persists cross-map unlocks via UMapSwitchSubsystem and triggers Server_TravelToMap . 

3. **Blueprint Interface** : SetupWidget , OnOkClicked . Bindings: ResultText , OkButton . 

4. **Component Architecture** : Modal UI. 

5. **Network/Replication** : Triggers server-side travel via Player Controller. 

### **UAbilityChooser** 

1. **Purpose** : Menu for customizing unit ability loadouts and spending ability points. 

2. **Implementation (CPP Analysis)** : Dynamically fetches buttons and icons by prefix (Offensive, Defensive, etc.). ClearAbilityArray empties specific sub-arrays ( SecondAbilities , ThirdAbilities , etc.) on the AAbilityUnit . UpdateAbilityDisplay syncs point 

totals. 

3. **Blueprint Interface** : StartUpdateTimer , StopTimer , InitWidget , SetOwnerActor , UpdateAbilityDisplay , SetAbilityIcons , SetVisibleAbilityButtonCount , ClearAbilityArray . 

4. **Component Architecture** : Polling-based update. 

5. **Network/Replication** : Local configuration that modifies replicated unit ability arrays. 

### **USelectorButton** 

https://wiki.teufel-engineering.com/en/rts-unit-template 

132/133 

9/27/26, 8:17 PM 

RTS Unit Template | Teufel Engineering Wiki 

1. **Purpose** : Interactive button used within selection grids to target specific units or toggle UI states. 

2. **Implementation (CPP Analysis)** : If SelectUnit is true, calls ControllerBase>SelectUnit(newID) . Otherwise, toggles unit-specific widgets via ControllerBase>SetWidgets(newID) . Updates parent UUnitWidgetSelector names and colors. 

3. **Blueprint Interface** : OnClick , SetUnitSelectorId . Properties: Id , Selector reference, SelectUnit (bool). 

4. **Component Architecture** : Functional component for HUD. 

5. **Network/Replication** : Triggers local selection logic. 

© 2026 Teufel-Engineering. All rights reserved. | Powered by Wiki.js 

Impressum Datenschutz 

https://wiki.teufel-engineering.com/en/rts-unit-template 

133/133 

