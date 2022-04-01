import kivy
from kivy.app import App
from kivy.uix.gridlayout import GridLayout
from kivy.uix.label import Label
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button


class ChildApp(GridLayout):     # here we have start give layout of our app
    def __init__(self, **kwargs):
        super(ChildApp, self).__init__()
        self.cols = 2                   # here we make 2 column
        self.add_widget(Label(text='Student Name'))   # here label name is this
        self.s_name = TextInput()           # here we  store variable name in this student name
        self.add_widget(self.s_name)      # here we add these function s_name

        # one more input we add here

        self.add_widget(Label(text='Student Marks'))
        self.s_marks = TextInput()
        self.add_widget(self.s_marks)

        self.add_widget(Label(text='Student Gender'))
        self.s_gender = TextInput()
        self.add_widget(self.s_gender)

        self.press = Button(text='Click Me')
        self.press.bind(on_press=self.click_me)
        self.add_widget(self.press)

    def click_me(self, instance):
        print('The name of student  is '+self.s_name.text)
        print('The marks of student is ' + self.s_marks.text)
        print('The gender of student is '+self.s_gender.text)
        print("")


class ParentApp(App):
    def build(self):
        return ChildApp()


if __name__ == "__main__":
    ParentApp().run()
