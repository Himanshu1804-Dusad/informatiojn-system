# informatiojn-system
1. Develop a web-based information system using basic technologies such as mark-up languages, stylesheets, JavaScript, PHP script, and databases
import { useState } from 'react'
import { BrowserRouter as Router, Link, Route, Routes } from 'react-router-dom'
import { Home, User, Music, Calendar, House, Menu } from 'lucide-react'
import { Card, CardContent, CardHeader, CardTitle } from "/components/ui/card"

// Mock data for the house information (replaces PHP array)
const houseInfo = [
  { key: 'Type', value: 'Apartment' },
  { key: 'Bedrooms', value: '2' },
  { key: 'Bathrooms', value: '1' },
  { key: 'Address', value: '123 Main Street, Cityville' },
  { key: 'Floor', value: '3rd' },
  { key: 'Square Footage', value: '850 sq ft' }
]

// Mock study subjects
const subjects = [
  'Web Development',
  'Database Systems',
  'Algorithms',
  'Computer Networks',
  'Software Engineering'
]

// Mock hobbies with images
const hobbies = [
  { name: 'Photography', image: '/hobby1.jpg' },
  { name: 'Hiking', image: '/hobby2.jpg' },
  { name: 'Reading', image: '/hobby3.jpg' },
  { name: 'Cooking', image: '/hobby4.jpg' }
]

// Mock music tracks
const musicTracks = [
  { 
    title: 'Bohemian Rhapsody', 
    artist: 'Queen', 
    artistLink: 'https://www.queenonline.com/',
    audio: '/audio/bohemian.mp3',
    video: '/video/bohemian.mp4'
  },
  { 
    title: 'Imagine', 
    artist: 'John Lennon', 
    artistLink: 'https://www.johnlennon.com/',
    audio: '/audio/imagine.mp3',
    video: '/video/imagine.mp4'
  },
  { 
    title: 'Thriller', 
    artist: 'Michael Jackson', 
    artistLink: 'https://www.michaeljackson.com/',
    audio: '/audio/thriller.mp3',
    video: '/video/thriller.mp4'
  }
]

// Mock news feed
const newsFeed = [
  'New album released by favorite artist',
  'Upcoming tech conference in the city',
  'Local hiking trails reopened after maintenance',
  'New cooking class starting next month'
]

// External links
const externalLinks = [
  { name: 'GitHub', url: 'https://github.com', icon: '/github-icon.jpg' },
  { name: 'LinkedIn', url: 'https://linkedin.com', icon: '/linkedin-icon.jpg' },
  { name: 'Stack Overflow', url: 'https://stackoverflow.com', icon: '/stackoverflow-icon.jpg' },
  { name: 'Medium', url: 'https://medium.com', icon: '/medium-icon.jpg' }
]

function Header() {
  return (
    <header className="bg-blue-600 text-white p-4 flex items-center justify-between">
      <div className="flex items-center space-x-4">
        <div className="bg-gray-200 border-2 border-dashed rounded-xl w-16 h-16" />
        <h1 className="text-2xl font-bold">My Personal Website</h1>
      </div>
      <nav className="hidden md:block">
        <ul className="flex space-x-6">
          <li><Link to="/" className="hover:underline flex items-center"><Home className="mr-1 h-4 w-4" /> Home</Link></li>
          <li><Link to="/study" className="hover:underline flex items-center"><User className="mr-1 h-4 w-4" /> My Study</Link></li>
          <li><Link to="/hobbies" className="hover:underline flex items-center"><User className="mr-1 h-4 w-4" /> My Hobbies</Link></li>
          <li><Link to="/music" className="hover:underline flex items-center"><Music className="mr-1 h-4 w-4" /> My Music</Link></li>
          <li><Link to="/house" className="hover:underline flex items-center"><House className="mr-1 h-4 w-4" /> My House</Link></li>
        </ul>
      </nav>
      <button className="md:hidden">
        <Menu className="h-6 w-6" />
      </button>
    </header>
  )
}

function Sidebar() {
  return (
    <aside className="w-full md:w-64 bg-gray-100 p-4">
      <h2 className="text-lg font-semibold mb-4">News Feed</h2>
      <ul className="space-y-2">
        {newsFeed.map((item, index) => (
          <li key={index} className="p-2 hover:bg-gray-200 rounded">{item}</li>
        ))}
      </ul>
      
      <h2 className="text-lg font-semibold mt-6 mb-4">External Links</h2>
      <ul className="space-y-2">
        {externalLinks.map((link, index) => (
          <li key={index} className="p-2 hover:bg-gray-200 rounded">
            <a href={link.url} target="_blank" rel="noopener noreferrer" className="flex items-center">
              {index >= 2 && <div className="bg-gray-200 border-2 border-dashed rounded-xl w-6 h-6 mr-2" />}
              {link.name}
            </a>
          </li>
        ))}
      </ul>
    </aside>
  )
}

function HomePage() {
  return (
    <div className="p-6">
      <Card>
        <CardHeader>
          <CardTitle>About Me</CardTitle>
        </CardHeader>
        <CardContent>
          <div className="flex flex-col md:flex-row gap-6">
            <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full md:w-64 h-64" />
            <div>
              <p className="mb-4">
                <strong>Hello!</strong> My name is Alex, and I'm a <em>passionate</em> web developer with 
                <u>5 years of experience</u> in creating modern, responsive websites. I specialize in 
                React, Node.js, and database design.
              </p>
              <hr className="my-4" />
              <p className="mb-4">
                My <strong>main achievements</strong> include developing a popular e-commerce platform 
                that serves over 10,000 users daily and receiving the <em>"Best Developer"</em> award 
                at my university. I'm constantly learning new technologies to stay at the <u>forefront</u> 
                of web development.
              </p>
              <hr className="my-4" />
              <p>
                My <strong>goals</strong> for the next year include mastering <em>advanced React patterns</em>, 
                contributing to open-source projects, and <u>launching</u> my own SaaS product. I believe 
                in continuous learning and sharing knowledge with the community.
              </p>
            </div>
          </div>
        </CardContent>
      </Card>
    </div>
  )
}

function StudyPage() {
  return (
    <div className="p-6">
      <Card>
        <CardHeader>
          <CardTitle>My Study Subjects</CardTitle>
        </CardHeader>
        <CardContent>
          <div className="mb-8">
            <h3 className="text-xl font-semibold mb-4">Current Subjects:</h3>
            <ol className="list-decimal pl-6 space-y-2">
              {subjects.map((subject, index) => (
                <li key={index}>{subject}</li>
              ))}
            </ol>
          </div>
          
          <div>
            <h3 className="text-xl font-semibold mb-4">Class Schedule:</h3>
            <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full h-64 mb-4" />
            
            <table className="min-w-full border">
              <thead>
                <tr className="bg-gray-100">
                  <th className="border p-2">Time</th>
                  <th className="border p-2">Monday</th>
                  <th className="border p-2">Tuesday</th>
                  <th className="border p-2">Wednesday</th>
                  <th className="border p-2">Thursday</th>
                  <th className="border p-2">Friday</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td className="border p-2">9:00-10:30</td>
                  <td className="border p-2">Web Development</td>
                  <td className="border p-2">Algorithms</td>
                  <td className="border p-2">Web Development</td>
                  <td className="border p-2">Database Systems</td>
                  <td className="border p-2">Software Engineering</td>
                </tr>
                <tr>
                  <td className="border p-2">11:00-12:30</td>
                  <td className="border p-2">Computer Networks</td>
                  <td className="border p-2">Web Development</td>
                  <td className="border p-2">Algorithms</td>
                  <td className="border p-2">Computer Networks</td>
                  <td className="border p-2">Database Systems</td>
                </tr>
                <tr>
                  <td className="border p-2">2:00-3:30</td>
                  <td className="border p-2">Database Systems</td>
                  <td className="border p-2">Software Engineering</td>
                  <td className="border p-2">Computer Networks</td>
                  <td className="border p-2">Algorithms</td>
                  <td className="border p-2">Web Development</td>
                </tr>
              </tbody>
            </table>
          </div>
        </CardContent>
      </Card>
    </div>
  )
}

function HobbiesPage() {
  return (
    <div className="p-6">
      <Card>
        <CardHeader>
          <CardTitle>My Hobbies</CardTitle>
        </CardHeader>
        <CardContent>
          <ul className="space-y-6">
            {hobbies.map((hobby, index) => (
              <li key={index} className="flex flex-col md:flex-row items-start gap-4">
                <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full md:w-48 h-48" />
                <div className="flex-1">
                  <h3 className="text-xl font-semibold">{hobby.name}</h3>
                  <p className="mt-2">
                    {hobby.name === 'Photography' && 'I enjoy capturing moments and landscapes with my DSLR camera.'}
                    {hobby.name === 'Hiking' && 'Exploring nature trails and mountains is my way to relax and stay fit.'}
                    {hobby.name === 'Reading' && 'I love reading science fiction and technical books in my free time.'}
                    {hobby.name === 'Cooking' && 'Experimenting with new recipes and cuisines is my creative outlet.'}
                  </p>
                </div>
              </li>
            ))}
          </ul>
        </CardContent>
      </Card>
    </div>
  )
}

function MusicPage() {
  return (
    <div className="p-6">
      <Card>
        <CardHeader>
          <CardTitle>My Music</CardTitle>
        </CardHeader>
        <CardContent>
          <div className="space-y-8">
            {musicTracks.map((track, index) => (
              <div key={index} className="border-b pb-6 last:border-b-0">
                <h3 className="text-xl font-semibold">{track.title}</h3>
                <p className="mb-4">
                  Artist: <a href={track.artistLink} target="_blank" rel="noopener noreferrer" className="text-blue-600 hover:underline">{track.artist}</a>
                </p>
                
                <div className="flex flex-col md:flex-row gap-4">
                  <div className="flex-1">
                    <h4 className="font-medium mb-2">Audio:</h4>
                    <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full h-16" />
                  </div>
                  <div className="flex-1">
                    <h4 className="font-medium mb-2">Video:</h4>
                    <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full h-48" />
                  </div>
                </div>
              </div>
            ))}
          </div>
        </CardContent>
      </Card>
    </div>
  )
}

function HousePage() {
  return (
    <div className="p-6">
      <Card>
        <CardHeader>
          <CardTitle>My House</CardTitle>
        </CardHeader>
        <CardContent>
          <div className="flex flex-col md:flex-row gap-6">
            <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full md:w-96 h-64" />
            <div className="flex-1">
              <table className="min-w-full border">
                <tbody>
                  {houseInfo.map((item, index) => (
                    <tr key={index} className={index % 2 === 0 ? 'bg-gray-50' : ''}>
                      <td className="border p-2 font-semibold">{item.key}</td>
                      <td className="border p-2">{item.value}</td>
                    </tr>
                  ))}
                </tbody>
              </table>
            </div>
          </div>
        </CardContent>
      </Card>
    </div>
  )
}

function Footer() {
  return (
    <footer className="bg-gray-800 text-white p-6">
      <div className="container mx-auto">
        <div className="flex flex-col md:flex-row justify-between items-center">
          <div className="mb-4 md:mb-0">
            <h3 className="text-lg font-semibold mb-2">Contact Information</h3>
            <p>Email: <a href="mailto:example@domain.com" className="hover:underline">example@domain.com</a></p>
            <p>Phone: (555) 123-4567</p>
            <p>
              Social: <a href="https://facebook.com" target="_blank" rel="noopener noreferrer" className="hover:underline">Facebook Profile</a>
            </p>
          </div>
          <div>
            <p>Site created on: {new Date().toLocaleDateString()}</p>
          </div>
        </div>
      </div>
    </footer>
  )
}

function App() {
  return (
    <div className="min-h-screen flex flex-col">
      <Header />
      <div className="flex flex-1">
        <Sidebar />
        <main className="flex-1">
          <Routes>
            <Route path="/" element={<HomePage />} />
            <Route path="/study" element={<StudyPage />} />
            <Route path="/hobbies" element={<HobbiesPage />} />
            <Route path="/music" element={<MusicPage />} />
            <Route path="/house" element={<HousePage />} />
          </Routes>
        </main>
      </div>
      <Footer />
    </div>
  )
}

export default function PersonalWebsite() {
  return (
    <Router>
      <App />
    </Router>
  )
}
