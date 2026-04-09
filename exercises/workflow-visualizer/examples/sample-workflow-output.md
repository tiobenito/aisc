# Sample Workflow Output: Content Approval Process

This describes what the visual diagram looks like for the content approval workflow described in `sample-workflow-description.md`. The actual output would be an Excalidraw file, SVG, or HTML diagram -- this document describes the structure for reference.

---

## Diagram structure

### Nodes (top to bottom, left to right)

1. **Start** (rounded rectangle) -- "Content Brief Assigned"
2. **Process** (rectangle) -- "Writer Creates Draft in Google Docs"
3. **Process** (rectangle) -- "Writer Moves Card to 'Ready for Review'"
4. **Decision** (diamond) -- "Content Lead Reviews"
   - **Yes path** (right/down) -- "Approved" -> continues to next step
   - **No path** (left/loop) -- "Needs Revisions" -> loops back to "Writer Creates Draft"
5. **Decision** (diamond) -- "Mentions Product Features or Pricing?"
   - **Yes path** (right) -- goes to "Product Team Sign-off"
   - **No path** (down) -- skips to "Design Team"
6. **Process** (rectangle) -- "Product Team Sign-off"
   - Connects back to main flow at "Design Team"
7. **Process** (rectangle) -- "Design Team Creates Visuals"
8. **Decision** (diamond) -- "Content Lead Final Review"
   - **Yes path** -- "Approved" -> continues
   - **No path** -- "Needs Changes" -> loops back to relevant step
9. **Process** (rectangle) -- "Schedule in CMS"
10. **Process** (rectangle) -- "Notify Team in Slack"
11. **End** (rounded rectangle) -- "Published"

### Visual details

- **Flow direction:** Top to bottom (primary), left to right (for branches)
- **Color coding:**
  - Blue rectangles -- manual human steps
  - Green rectangles -- automated/system steps (CMS scheduling, Slack notification)
  - Yellow diamonds -- decision points
  - Gray rounded rectangles -- start/end
- **Arrows:** Solid lines with arrowheads. Decision branches labeled "Yes"/"No" or "Approved"/"Needs Revisions"
- **Swim lanes (optional refinement):** Columns for Writer, Content Lead, Design Team, Product Team -- showing who owns each step

### What makes this a good diagram

- Every step has a clear owner (implied by position or label)
- Decision points show both paths, including what happens on rejection
- The loop-back arrows make the revision cycle visible
- The conditional branch (product sign-off) shows it's not always required
- Start and end are clearly marked
