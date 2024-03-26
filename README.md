# AI-driven-Mental-Health-Support
Entwickeln Sie eine KI-gesteuerte Plattform zur Unterstützung der psychischen Gesundheit, die personalisierte Ressourcen und Selbsthilfe-Tools bereitstellt.
import random

# Simulated database of resources
RESOURCES = {
    "stress": ["Mindfulness for Stress Reduction", "Time Management Strategies"],
    "anxiety": ["Coping with Anxiety", "Breathing Techniques for Relaxation"],
    "depression": ["Finding Joy: Activities to Boost Your Mood", "Connecting with Others: Overcoming Isolation"],
}

# Basic AI model simulation
def get_resources_for_issue(issue):
    """Simulate an AI model to recommend resources based on the user's issue."""
    keywords = issue.lower().split()
    recommended_resources = []
    for keyword in keywords:
        if keyword in RESOURCES:
            recommended_resources.extend(RESOURCES[keyword])
    if not recommended_resources:
        return ["We're sorry, but we don't have specific resources for this issue. Please consult a professional."]
    return recommended_resources

def ai_driven_mental_health_support():
    """Main function to interact with the user and provide personalized mental health support resources."""
    print("Welcome to the AI-driven Mental Health Support platform.")
    print("Please tell us what you're feeling or going through, and we'll suggest some resources that might help.")
    
    user_input = input("Your issue: ").strip()
    if not user_input:
        print("It seems like you didn't enter an issue. Please try again.")
        return
    
    print("\nAnalyzing your input...")
    # Simulating a brief delay
    recommended_resources = get_resources_for_issue(user_input)
    
    print("\nBased on what you've told us, you might find the following resources helpful:")
    for resource in recommended_resources:
        print("- ", resource)

# Run the demo
if __name__ == "__main__":
    ai_driven_mental_health_support()
