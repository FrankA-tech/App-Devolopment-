!-- UserProfilePage.xaml -->
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TechNetworkingApp.UserProfilePage"
             Title="User Profile">

    <StackLayout Padding="10">
        <Image Source="profile_placeholder.png" HeightRequest="100" WidthRequest="100" HorizontalOptions="Center"/>
        <Label Text="Name" FontSize="Medium" />
        <Entry x:Name="NameEntry" Placeholder="Enter your name" />
        
        <Label Text="Email" FontSize="Medium" />
        <Entry x:Name="EmailEntry" Placeholder="Enter your email" Keyboard="Email" />
        
        <Label Text="Skills" FontSize="Medium" />
        <Editor x:Name="SkillsEditor" Placeholder="Enter your skills" HeightRequest="100" />
        
        <Button Text="Save" Clicked="OnSaveButtonClicked" />
    </StackLayout>
</ContentPage>
// UserProfilePage.xaml.cs
using Xamarin.Forms;

namespace TechNetworkingApp
{
    public partial class UserProfilePage : ContentPage
    {
        public UserProfilePage()
        {
            InitializeComponent();
        }

        private void OnSaveButtonClicked(object sender, EventArgs e)
        {
            string name = NameEntry.Text;
            string email = EmailEntry.Text;
            string skills = SkillsEditor.Text;

            // Save the user profile information (e.g., to a database or cloud service)
            DisplayAlert("Profile Saved", "Your profile has been saved successfully.", "OK");
        }
    }
}
<!-- MainPage.xaml -->
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="TechNetworkingApp.MainPage"
             Title="Home">

    <StackLayout Padding="10">
        <Button Text="Go to Profile" Clicked="OnProfileButtonClicked" />
    </StackLayout>
</ContentPage>
// MainPage.xaml.cs
using Xamarin.Forms;

namespace TechNetworkingApp
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
        }

        private async void OnProfileButtonClicked(object sender, EventArgs e)
        {
            await Navigation.PushAsync(new UserProfilePage());
        }
    }
}
