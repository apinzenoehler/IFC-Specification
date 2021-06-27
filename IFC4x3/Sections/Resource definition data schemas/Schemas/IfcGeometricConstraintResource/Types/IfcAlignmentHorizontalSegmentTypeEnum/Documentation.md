<style>
td {
  font-size: small
}
th {
  font-size: small
}
</style>

The IfcAlignmentHorizontalSegmentTypeEnum indicates the type of a segment of a horizontal alignment segment (IfcAlignmentHorizontalSegment). Horizontal segments can be viewed from a geometric perspective and from a kinematic perspective. In recent times the kinematic perspective gained importance. The enumerations are detailed according to this development especially in modern track design.

### kinematic perspective on horizontal alignment segments

The central parameter of the horizontal design is the curvature of the segment. According to the curvature value the following categorization can be made:


| Curvature | Segmenttype        | Enumeration Values |
|:----|:------------------|:----------|
| 0 | straight line        | LINE |
| constant in the complete segment, <> 0 | Circular arc  | CIRCULARARC |
| variation along the segment | Transition with linear curvature variation | CLOTHOID, CUBIC  |
| variation along the segment | Transition with non-linear curvature variation | HELMERTCURVE, BLOSSCURVE, COSINECURVE, SINECURVE, VIENNESEBEND |


### geometric perspective on horizontal alignment segments



The geometric perspective denotes in the context of the business terminology related IfcAlignment documentation the traditional view. Before the availability of modern computers alignment design was performed using "traditional" drawing techniques. In the first phase of computerization this origin led to a representation in the x,y space first and a check of safety related properties in a second step. This can still be seen in regulations which have been put into effect 1980 or earlier. Of course designs which have been produced on basis of these regulations reflect the "good enough" attitude in the precision of the documentation. 

In a later phase an increasing importance of the kinematic perspective can be observed. Here precise control of the lateral acceleration (horizontal and cant layout) and vertical acceleration (vertical layout) became prevalent. Designers started to use high performance transition bends especially in high speed scenarios. In the kinematic perspective precise curvature fitting between consecutive segments needs to be better than in the "good enough" approach of traditional geometric perspective. Central terms are e.g. "jerks", "theoretical cant" or "cant deficiency".

### Word or warning

"Good enough" traditional designs have to be carefully checked before being included into a high precision 3D model. Intermediate corrections might be necessary. Fortunately the clothoid works very well with comparable documentation quality both in the classic geometric perspective and in the more recent kinematic perspective. Fortunately the huge majority of horizontal transition bends are designed and implemented as clothoids.

### Recommendation

Check the relevant regulations for the network in question. Alignment designs as such are very stable over the livetime of the road or track. Especially for old designs quality and precision of available documentation has to be checked very carefully. A clear understanding of limitations should be established before implementing automated data flows between high precision BIM environments and legacy documentation systems. This applies both to legacy, central databases and to legacy, individual documents. 

### Used Symbols and their meaning

| Symbol | meaning  | Unit, value range |
|:----|:------------------|:----------|
| L | full length of segment        | positive length  L > 0 |
| s | current position on segment        | 0 < s < L |
| &xi;  | $ = s / L$ (Greek "xi") standardised, dimensionless path length along the alignment / track centre line        | 0 < &xi; < 1 |
|  &kappa; | (Greek "kappa") Curvature (inverse radius) of the alignment / track centre line in plan view (horizontal layout).        | 1/radius  |
| &kappa;<sub>1</sub> | Curvature (inverse radius) at beginning of the alignment / track centre line in plan view (horizontal layout).        | 1/radius  |
| &psi; | (Greek "psi") Angle of cant (cross slope angle, bank angle)        | rad |
