Anime
Anime analysis
import matplotlib.pyplot as plt

# Data for the visualizations
page_views = [15000, 10000, 12000]  # Hypothetical views for three articles
bounce_rates = [65, 55, 50]  # Hypothetical bounce rates

# Creating bar chart for page views and bounce rate
fig, ax1 = plt.subplots(figsize=(10, 6))

ax1.bar(['Tower of God', 'Refund High School', 'Solo Leveling'], page_views, color='blue', alpha=0.6, label='Page Views')
ax1.set_xlabel('Articles')
ax1.set_ylabel('Page Views', color='blue')
ax1.tick_params(axis='y', labelcolor='blue')

# Create another axis for the bounce rates
ax2 = ax1.twinx()
ax2.plot(['Tower of God', 'Refund High School', 'Solo Leveling'], bounce_rates, color='red', marker='o', label='Bounce Rate')
ax2.set_ylabel('Bounce Rate (%)', color='red')
ax2.tick_params(axis='y', labelcolor='red')

# Add titles and labels
plt.title('Page Views and Bounce Rate Comparison')
ax1.legend(loc='upper left')
ax2.legend(loc='upper right')

# Show the combined plot
plt.tight_layout()
plt.show()


# Data for the pie chart (Hypothetical time spent categories for "Tower of God")
time_spent_distribution = [30, 40, 20, 10]  # Percentages for time spent categories
labels = ['< 1 min', '1-2 min', '2-3 min', '> 3 min']
colors = ['#ff9999','#66b3ff','#99ff99','#ffcc99']

# Creating pie chart
fig, ax = plt.subplots(figsize=(7, 7))
ax.pie(time_spent_distribution, labels=labels, autopct='%1.1f%%', startangle=90, colors=colors, explode=(0.05, 0, 0, 0))
ax.axis('equal')  # Equal aspect ratio ensures that pie is drawn as a circle.
plt.title('Time Spent on "Tower of God" Article')

# Show the pie chart
plt.tight_layout()
plt.show()
