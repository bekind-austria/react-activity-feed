```js
const activities = [
  {
    actor: {
      data: {
        name: 'Jaap Bakker',
        profileImage: 'https://randomuser.me/api/portraits/men/72.jpg',
      },
    },
    verb: 'follow',
    object: {
      verb: 'post',
      object:
        'Winds 2 is the Open Source megalocosmos flat earth effect of anti-gravity food chemicals...',
      actor: {
        data: {
          name: 'Josh',
        },
      },
    },
    time: Date.now() - 1000000,
  },
  {
    actor: {
      data: {
        name: 'Jaap Bakker',
        profileImage: 'https://randomuser.me/api/portraits/women/72.jpg',
      },
    },
    verb: 'heart',
    object: {
      verb: 'post',
    },
  },
  {
    actor: {
      data: {
        name: 'Jaap Bakker',
        profileImage: 'https://randomuser.me/api/portraits/women/7.jpg',
      },
    },
    verb: 'heart',
    object: {
      verb: 'post',
    },
  },
];

const unreadGroup = {
  read: false,
  activities,
};

const readGroup = {
  read: true,
  activities,
};

<div style={{ padding: 20, backgroundColor: 'grey' }}>
  <DropdownPanel
    arrow
    Header={
      <React.Fragment>
        <div
          style={{
            display: 'flex',
            justifyContent: 'space-between',
            alignItems: 'center',
            padding: 10,
          }}
        >
          <Title size={14}>Notifications</Title>
          <Link>Mark as read</Link>
        </div>
        <NewActivitiesNotification adds={[{}, {}, {}, {}, {}]} />
      </React.Fragment>
    }
    Footer={
      <div
        style={{
          display: 'flex',
          padding: 10,
          alignItems: 'center',
          justifyContent: 'center',
        }}
      >
        <Link to="#">View All Notifications</Link>
      </div>
    }
  >
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={unreadGroup} />
    <Notification activityGroup={readGroup} />
    <Notification activityGroup={readGroup} />
    <Notification activityGroup={readGroup} />
    <Notification activityGroup={readGroup} />
  </DropdownPanel>
</div>;
```
