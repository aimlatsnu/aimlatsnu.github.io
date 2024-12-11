--- 

---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Applications Group - Shiv Nadar University</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">AI Group - SNU</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#publications">Publications</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#people">People</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#events">Events</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container mt-5">
        <!-- Publications Section -->
        <section id="publications">
            <h2 class="mb-4">Publications</h2>
            {% assign sorted_publications = site.data.publications | sort: "year" | reverse %}
            <ul class="list-group">
                {% for pub in sorted_publications %}
                <li class="list-group-item">
                    <strong>{{ pub.title }}</strong> - {{ pub.year }}<br>
                    Authors: {{ pub.authors | join: ", " }}<br>
                    {% if pub.journal %}Journal: {{ pub.journal }}{% endif %}
                    {% if pub.conference %}Conference: {{ pub.conference }}{% endif %}
                    <br><a href="{{ pub.link }}" target="_blank">Read more</a>
                </li>
                {% endfor %}
            </ul>
        </section>

        <hr class="my-5">

        <!-- People Section -->
        <section id="people">
            <h2 class="mb-4">People</h2>
            <div class="row">
                <div class="col-md-4 text-center">
                    <img src="profile1.jpg" alt="Faculty Member 1" class="img-fluid rounded-circle mb-2" style="width: 150px; height: 150px;">
                    <h5>Dr. Faculty Member 1</h5>
                    <p>Specialization in AI applications</p>
                </div>
                <div class="col-md-4 text-center">
                    <img src="profile2.jpg" alt="Faculty Member 2" class="img-fluid rounded-circle mb-2" style="width: 150px; height: 150px;">
                    <h5>Dr. Faculty Member 2</h5>
                    <p>Specialization in Machine Learning</p>
                </div>
                <div class="col-md-4 text-center">
                    <img src="profile3.jpg" alt="Faculty Member 3" class="img-fluid rounded-circle mb-2" style="width: 150px; height: 150px;">
                    <h5>Dr. Faculty Member 3</h5>
                    <p>Specialization in Natural Language Processing</p>
                </div>
                <!-- Add more faculty profiles as needed -->
            </div>
        </section>

        <hr class="my-5">

        <!-- Events Section -->
        <section id="events">
            <h2 class="mb-4">Events</h2>
            <ul class="list-group">
                <li class="list-group-item">Event 1: Description and date...</li>
                <li class="list-group-item">Event 2: Description and date...</li>
                <li class="list-group-item">Event 3: Description and date...</li>
                <!-- Add more events as needed -->
            </ul>
        </section>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
