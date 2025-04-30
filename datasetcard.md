**Dataset title:** Independent project for investigation of urbanization impacting genetic diversity in the San Francisco Bay Area

**Dataset curator:** Adriel Evaristo, Boria Lab at SFSU

## Dataset Summary
How does urbanization affect populations? Urbanization is reshaping ecosystems globally, influencing species’
diversity patterns. Urban areas have a higher presence of non-native species and decrease in the abundance
and diversity of native species. These environmental changes due to urbanization are creating new small
populations in small habitats, with unknown impacts on the evolution of life (Johnson and Munshi-South et
al. 2016). By looking at the San Francisco Bay Area through cities in San Francisco, Oakland, San Jose, and
Marin County. There are few studies of how the impact of urbanization is affecting these small habitats to
small mammal species, specifically the Peromyscus species. Habitat fragmentation threatens small habitats
in the San Francisco Bay, reducing genetic diversity and connectivity among populations (Wood et al., 2016).
There are different microclimates throughout parts of the Bay Area, allowing us to further discover how they
are affecting the Peromyscus species through urbanization. Using small mammals and next-gen sequencing
will determine if urbanization in the Bay Area, which includes San Francisco, San Jose, Oakland, and Marin
County, is causing evolutionary responses to the Peromyscus maniculatus

## Preliminary Results
Since we don't have full results from our project, I decided to do a hypothetical dataset of how it will look like if we captured mice around different sections of the San Francisco Bay Area.

Here's a hypothetical dataset of captured mice in different sections of the San Francisco Bay Area. Each row represents a unique mouse capture event, and the data includes details such as:

Capture ID
Location (San Francisco, Oakland, San Mateo, Marin County)
Date Captured
Species (e.g., Deer Mouse, House Mouse, Field Mouse)
Weight (grams)
Sex
Age Category (Juvenile, Subadult, Adult)

## Preliminary Dataset
|Capture ID|	|Location|	|Date Captured|	|Species	Weight (g)|	|Sex	Age Category|
|SF001|	|San Francisco|	|2025-03-14|	|House Mouse|	|18|	|Male|	|Adult|
|SF002|	|San Francisco|	|2025-03-16|	|Deer Mouse|	|22|	|Female|	|Subadult|
|SF003|	|San Francisco|	|2025-03-18|	|House Mouse|	|16|	|Female|	|Juvenile|
|SF004|	|San Francisco|	|2025-03-20|	|Deer Mouse|	|21|	|Male|	|Subadult|
|SF005|	|San Francisco|	|2025-03-21|	|House Mouse|	|16|	|Male|	|Juvenile|
|OAK001|	|Oakland|	|2025-03-12|	|Field Mouse|	20|	|Male|	|Adult|
|OAK002|	|Oakland|	|2025-03-13|	|House Mouse|	17|	|Female|	|Subadult|
|OAK003|	|Oakland|	|2025-03-15|	|Deer Mouse|	|25|	|Male|	|Adult|
|OAK004|	|Oakland|	|2025-03-16|	|House Mouse|	|15|	|Female|	|Juvenile|
|OAK005|	|Oakland|	|2025-03-19|	|Field Mouse|	|23|	|Male|	|Adult|
|SM001|	|San Mateo|	|2025-03-11|	|Field Mouse|	|21|	|Male|	|Adult|
|SM002|	|San Mateo|	|2025-03-13|	|House Mouse|	|19|	|Male|	|Subadult|
|SM003|	|San Mateo|	|2025-03-17|	|House Mouse|	|14|	|Female|	|Juvenile|
|SM004|	|San Mateo|	|2025-03-18|	|Deer Mouse|	|23|	|Female|	|Adult|
|SM005|	|San Mateo|	|2025-03-20|	|House Mouse|	|18|	|Female|	|Subadult|
|MAR001|	|Marin County|	|2025-03-10|	|Field Mouse|	|24|	|Male|	|Adult|
|MAR002|	|Marin County|	|2025-03-12|	|Deer Mouse|	|20|	|Female|	|Subadult|
|MAR003|	|Marin County|	|2025-03-13|	|House Mouse|	|15|	|Male|	|Juvenile|
|MAR004|	|Marin County|	|2025-03-15|	|Field Mouse|	|22|	|Female|	|Adult|
|MAR005|	|Marin County|	|2025-03-21|	|Deer Mouse|	|19|	|Female|	|Juvenile|

```{r}
# 1 Import Data
library(readr)
mice_captures <- read_csv("Downloads/mice_captures.csv")
View(mice_captures)
```

```{r}
# Histogram and Boxplot
# Box plot of Weight by Location
ggplot(mice_data, aes(x = Location, y = `Weight (g)`, fill = Location)) +
  geom_boxplot() +
  labs(title = "Box Plot of Mouse Weight by Location",
       x = "Location",
       y = "Weight (g)")
```

```{r}
# Histogram of Mouse Weights
ggplot(mice_data, aes(x = `Weight (g)`)) +
  geom_histogram(binwidth = 2) +
  labs(title = "Histogram of Mouse Weights",
       x = "Weight (g)",
       y = "Count")
```

